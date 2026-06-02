# 🗂️ Project Kumquat — Notion Database Blueprint

**The Interactive Digital Workspace Tier.** This document is a build specification. Follow it top-to-bottom to construct a self-study dashboard in Notion that tracks the entire **~114-hour** curriculum, logs every study session, and renders progress as Kanban boards.

> **Architecture in one line:** two linked databases — a **Curriculum Tracker** (the 15 modules) and a **Study Session Log** (your time entries) — joined by a Relation, with **Hours Spent** rolled up automatically.

---

## 0. System Overview

```text
   +---------------------------+         Relation        +-------------------------+
   |   DB 1: Curriculum Tracker | 1 ----------------< many |  DB 2: Study Session Log |
   |   (15 module cards)        |                          |  (one row per session)   |
   +---------------------------+                          +-------------------------+
            |   ^                                                     |
            |   |  Rollup: SUM(Session Hours)  <----------------------+
            v   |
     Kanban by Status / Phase / Priority
```

- **DB 1 — Curriculum Tracker:** the master board. One card per module (15 total).
- **DB 2 — Study Session Log:** every time you sit down to study, you add a row here.
- **The link:** each Session points to one Module. A **Rollup** on the Module sums its sessions into **Hours Spent**, and a **Formula** turns that into a **Progress %**.

---

## 1. Database 1 — "Kumquat · Curriculum Tracker"

Create a new database (full page). Add these properties **exactly**.

| Property | Type | Configuration / Options | Purpose |
| :--- | :--- | :--- | :--- |
| **Module** | Title | e.g. `2.3 Immune Wipe: Feline Panleukopenia` | Primary key / card title |
| **Status** | Select | `🔲 Not Started` · `🔄 In Progress` · `⛔ Blocked` · `🔍 Review` · `✅ Done` | Kanban driver |
| **Phase** | Select | `🟢 Phase 1` · `🟠 Phase 2` · `🔴 Phase 3` | Grouping & color |
| **Priority** | Select | `🔥 Critical` · `⬆ High` · `▶ Normal` · `⬇ Low` | Triage of study order |
| **Materials** | Files & media / URL | Paste verified `resource_urls` from `CURRICULUM_MATRIX.json` | One click to the source |
| **Est. Hours** | Number | Integer (from the matrix) | Planned load |
| **Hours Spent** | Rollup | Rollup → relation **Sessions**, property **Session Hours**, calculate **Sum** | Actual load (auto) |
| **Progress** | Formula | see §4 | Visual % bar |
| **Bilingual Keywords** | Multi-select | EN / AR term pairs (see seed table) | Vocabulary drill |
| **Engineering Analogue** | Text | The hardware-stack framing | Keeps the philosophy in view |
| **Exit Objective** | Text | The measurable exit criterion | Definition of done |
| **Sessions** | Relation | Relation → **Study Session Log** (two-way) | Links time entries |

---

## 2. Database 2 — "Kumquat · Study Session Log"

Create a second database. Properties:

| Property | Type | Configuration / Options | Purpose |
| :--- | :--- | :--- | :--- |
| **Session** | Title | e.g. `2026-06-03 · 2.3 deep dive` | Row label |
| **Date** | Date | Include time (optional) | Calendar view |
| **Module** | Relation | Relation → **Curriculum Tracker** | The other half of the link |
| **Session Hours** | Number | Decimal (e.g. `1.5`) | Feeds the Rollup |
| **Focus** | Text | What you actually covered | Recall anchor |
| **Confidence** | Select | `1 · Fog` · `2 · Shaky` · `3 · Okay` · `4 · Solid` · `5 · Could teach it` | Self-assessment |
| **Blocker?** | Checkbox | Tick if something stalled you | Surfaces friction |
| **Notes** | Text | Free-form log | Spaced-repetition fuel |

---

## 3. Kanban Board Structures (Views)

Build these **views** on top of the two databases.

### View A — "Mission Control" (Board, on DB 1)

- **Layout:** Board
- **Group by:** `Status`
- **Columns (left → right):** `🔲 Not Started → 🔄 In Progress → ⛔ Blocked → 🔍 Review → ✅ Done`
- **Card preview:** show `Phase`, `Priority`, `Progress`, `Est. Hours`
- **Sort:** `Priority` descending, then `Module` ascending

```text
  NOT STARTED      IN PROGRESS      BLOCKED        REVIEW         DONE
  +----------+     +----------+     +--------+     +--------+     +--------+
  | 1.3      |     | 2.3 🔥   |     | 2.4    |     | 1.5    |     | 1.1 ✅ |
  | 1.4      |     |  ▓▓▓░░ 60%|     |  wait  |     | ▓▓▓▓░  |     | 1.2 ✅ |
  +----------+     +----------+     +--------+     +--------+     +--------+
```

### View B — "Phase Pipeline" (Board, on DB 1)

- **Layout:** Board · **Group by:** `Phase`
- Three columns: `🟢 Phase 1 · 🟠 Phase 2 · 🔴 Phase 3`
- Use this to confirm you are **not** skipping the spec sheet (Phase 1 first).

### View C — "Triage Queue" (Board, on DB 1)

- **Layout:** Board · **Group by:** `Priority`
- Surfaces `🔥 Critical` modules (e.g. **2.3 Panleukopenia**, **3.4 CRT**, **3.5 Shock**) at the front.

### View D — "Study Calendar" (Calendar, on DB 2)

- **Layout:** Calendar · **Date by:** `Date`
- See your session cadence; spot gaps in the streak.

### View E — "Master Table" (Table, on DB 1)

- **Layout:** Table · show every property
- Add a **filter** `Status is not ✅ Done` for a clean "what's left" list.

---

## 4. Formulas

### Progress bar (DB 1 → property **Progress**, type Formula)

```notion
round(min(prop("Hours Spent") / prop("Est. Hours"), 1) * 100)
```

For a visual bar instead of a number, use:

```notion
slice("▓▓▓▓▓▓▓▓▓▓", 0, floor(min(prop("Hours Spent") / prop("Est. Hours"), 1) * 10)) +
slice("░░░░░░░░░░", 0, 10 - floor(min(prop("Hours Spent") / prop("Est. Hours"), 1) * 10)) +
" " + format(round(min(prop("Hours Spent") / prop("Est. Hours"), 1) * 100)) + "%"
```

### Auto-flag overrun (optional helper formula)

```notion
if(prop("Hours Spent") > prop("Est. Hours"), "⚠ Over budget", "on track")
```

---

## 5. Study Session Log — Markdown Template

Paste this into a **Template button** (DB 2 → "New template") so every session starts pre-formatted. Replace bracketed fields.

```markdown
### 🗓️ [YYYY-MM-DD] · Module [#.#] — [Module Title]

**Phase:** [🟢/🟠/🔴 Phase #]   **Session Hours:** [#.#]   **Confidence:** [1–5]

**Focus today**
- [ ] [Concept / milestone targeted]
- [ ] [Concept / milestone targeted]

**Bilingual terms drilled**
- [EN term] / [AR term]
- [EN term] / [AR term]

**Crash-log / what clicked**
- [One thing I now understand that I didn't before]

**Blocker?**  [none] / [describe — what stalled me]

**Next session starts with**
- [Smallest next action]
```

### Quick "field-debug" log variant (for Phase 3 practice)

```markdown
### 🔴 Triage Drill · [YYYY-MM-DD]

- **A — Airway:** [clear / obstructed → action]
- **B — Breathing:** [effective / supported]
- **T — Temperature:** [value °C → warm/cool]
- **C — CRT / gums:** [<2s pink / >2s pale → action]
- **F — Fluid status:** [stable / collapse → action]
- **Handoff note drafted?** [yes / no]
```

---

## 6. Seed Data — Import the 15 Modules

Paste this table into the **Curriculum Tracker** (Notion converts a Markdown table into rows, or import the CSV exported from `CURRICULUM_MATRIX.json`). Status defaults to `🔲 Not Started`.

| Module | Phase | Priority | Est. Hours | Key Bilingual Keywords |
| :--- | :--- | :--- | :---: | :--- |
| 1.1 The Hardware Stack Overview | 🟢 Phase 1 | ▶ Normal | 6 | Anatomy / التشريح · Homeostasis / الاتزان الداخلي |
| 1.2 Cellular Production Plants: Bone Marrow | 🟢 Phase 1 | ⬆ High | 8 | Bone marrow / نخاع العظم · Hematopoiesis / تكوين الدم |
| 1.3 The Lymphatic Transit Network | 🟢 Phase 1 | ▶ Normal | 8 | Lymphatic system / الجهاز اللمفاوي |
| 1.4 Localized Filter Checkpoints: Lymph Nodes | 🟢 Phase 1 | ▶ Normal | 6 | Lymph node / عقدة ليمفاوية · Antigen / مستضد |
| 1.5 Healthy Operating Parameters | 🟢 Phase 1 | ⬆ High | 8 | Vital signs / العلامات الحيوية · CRT / زمن امتلاء الشعيرات الدموية |
| 2.1 Threat Model: Viral · Bacterial · Toxic | 🟠 Phase 2 | ⬆ High | 8 | Pathogen / العامل الممرض · Toxin / السموم |
| 2.2 Code-Injection Mechanics | 🟠 Phase 2 | ⬆ High | 10 | Viral replication / التكاثر الفيروسي · Host cell / الخلية المضيفة |
| 2.3 Immune Wipe: Feline Panleukopenia | 🟠 Phase 2 | 🔥 Critical | 12 | Feline panleukopenia / طاعون القطط الفيروسي |
| 2.4 Gut-Barrier Breach & Bacterial Translocation | 🟠 Phase 2 | ⬆ High | 8 | Intestinal barrier / حاجز الأمعاء |
| 2.5 Cascade Failure: Sepsis & Liver Shutdown | 🟠 Phase 2 | ⬆ High | 10 | Sepsis / الإنتان · Liver failure / فشل الكبد |
| 3.1 The Deterministic Triage Loop | 🔴 Phase 3 | 🔥 Critical | 4 | Field triage / الفرز الميداني |
| 3.2 Airway & Breathing Subsystem Check | 🔴 Phase 3 | 🔥 Critical | 6 | Airway / مجرى الهواء · Breathing / التنفس |
| 3.3 Thermal Defense | 🔴 Phase 3 | ⬆ High | 6 | Hypothermia / انخفاض حرارة الجسم |
| 3.4 Perfusion Debug: Capillary Refill Time | 🔴 Phase 3 | 🔥 Critical | 6 | Perfusion / التروية · Gums / اللثة |
| 3.5 Fluid Collapse & Shock → Handoff | 🔴 Phase 3 | 🔥 Critical | 8 | Shock / الصدمة · Fluid therapy / العلاج بالسوائل |

---

## 7. Build Checklist

1. **Create DB 1** (Curriculum Tracker) with all properties from §1.
2. **Create DB 2** (Study Session Log) with all properties from §2.
3. **Link them:** add the **Sessions** relation (DB 1) ↔ **Module** relation (DB 2) — Notion creates the two-way link automatically.
4. **Add the Rollup** `Hours Spent` (§1) and the **Progress** formula (§4).
5. **Paste the seed table** (§6) into DB 1.
6. **Attach materials:** drop the verified `resource_urls` from `CURRICULUM_MATRIX.json` into each card's **Materials**.
7. **Build the five views** (§3): Mission Control, Phase Pipeline, Triage Queue, Study Calendar, Master Table.
8. **Add the template button** (§5) to DB 2 for one-click session logging.

> **Definition of done for the workspace:** opening Notion shows a Kanban where dragging a card to `✅ Done` is earned only when its **Exit Objective** is met and **Progress** reads 100%.

---

### 🍊 _Track the debug. Log every session. Stabilize, document, hand off._
