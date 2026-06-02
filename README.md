<div align="center">

# 🐾 The Engineer's Blueprint for Veterinary Medicine & Stray Triage

### **Project Kumquat** · Codename `KUMQUAT` · _Vet-level grounding for non-vets_

**Debug the animal. Don't guess it.**

![Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-CC--BY--SA--4.0-blue)
![Phases](https://img.shields.io/badge/phases-3-orange)
![Study%20Load](https://img.shields.io/badge/study%20load-~114h-yellow)
![Languages](https://img.shields.io/badge/lang-EN%20%2B%20AR%20%D8%B9%D8%B1%D8%A8%D9%8A-9cf)
![Audience](https://img.shields.io/badge/audience-rescuers%20%7C%20responders%20%7C%20bio--engineers-lightgrey)
![Not%20A%20DVM](https://img.shields.io/badge/⚠️-NOT%20a%20substitute%20for%20a%20DVM-red)

</div>

---

## 📡 Signal — Read This First

**Project Kumquat is an open-source education roadmap that maps veterinary science through an engineering lens.**

We reject dense, traditional medical literature. Instead, we model the animal body as a **complex hardware stack**: organs are specialized **sub-routines**, the vascular network is **fluid plumbing**, and the immune system is a dynamic, **multi-tier firewall**. When a biological system undergoes crisis, we do not guess — we **debug** using system block diagrams, logic trees, and fault-tree diagnostic protocols.

This repository is engineered for people who require **high-fidelity, academically grounded veterinary knowledge** — field rescuers, wildlife emergency responders, and bio-engineers — **without** navigating a full clinical licensing array.

---

## 🕯️ Acknowledgements

> Project Kumquat was born out of a critical baseline breakdown. When a tiny, vulnerable ginger kitten was rescued from an industrial zone, we encountered the unforgiving, hardcoded realities of nature: a fast-moving, hostile pathogen known as Feline Panleukopenia (طاعون القطط الفيروسي). In the field, time translates directly to survival. Traditional veterinary resources are locked behind dense, academic text walls that fail to serve rescuers, software engineers, and logical problem-solvers who require deterministic triage frameworks under pressure. This project honors the memory of that tiny fighter, Kumquat (affectionately known as Koki). It rejects unstructured medical literature in favor of a System Architecture Approach to Biology. We treat the animal body as an integrated hardware stack: organs are specialized sub-routines, the vascular network is fluid plumbing, and the immune system is a dynamic, multi-tier fire-wall. When a system goes down, we do not guess—we debug.

> _In memory of **Kumquat (Koki)** 🍊 — the baseline that taught us the cost of latency._

---

## 🎯 Who This Is For (and Who It Is Not)

| ✅ This curriculum **is** for | ❌ This curriculum **is not** |
| :--- | :--- |
| Field rescuers stabilizing animals before handoff | A replacement for a licensed **Doctor of Veterinary Medicine (DVM)** |
| Wildlife & disaster emergency responders | A casual pet-owner blog or "home remedy" guide |
| Bio-engineers and systems thinkers entering animal health | A licensing pathway or clinical certification |
| Logical problem-solvers who need deterministic frameworks | A source of drug dosages to administer without a vet |

> ⚠️ **GROUNDING GUARDRAIL.** Project Kumquat does **not** replace a licensed DVM degree. It provides **vet-level grounding for non-vets**. Every triage path in this project terminates at the same instruction: **stabilize, then hand off to a professional veterinarian.** Nothing here authorizes diagnosis, prescription, or surgery.

---

## 🧬 The Core Abstraction — Biology as a Hardware Stack

We hold one mapping consistent across **every** file in this repository. Learn the mapping once; reuse it everywhere.

| Biological System | Engineering Analogue | Arabic Term |
| :--- | :--- | :--- |
| **Bone marrow** | Cellular production plant / white-cell (WBC) factory | نخاع العظم |
| **Lymphatic system** | Transit network / internal message bus | الجهاز اللمفاوي |
| **Lymph node** | Localized filter checkpoint / firewall node | عقدة ليمفاوية |
| **Immune system** | Dynamic, multi-tier firewall | الجهاز المناعي |
| **Vascular network** | Fluid plumbing / pressurized pipework | الجهاز الدوراني |
| **Liver** | Detox & waste-processing daemon | الكبد |
| **Gut barrier** | Perimeter wall / I/O membrane | حاجز الأمعاء |
| **Mucous membranes / gums** | Status LEDs (perfusion & oxygenation readout) | الأغشية المخاطية |

---

## 🗺️ The 3-Phase Curriculum Core

Every asset in this project — Markdown, JSON, Notion schema, Marp slides, and the LaTeX thesis — maps strictly onto these three phases.

```
   PHASE 1 ───────────────▶ PHASE 2 ───────────────▶ PHASE 3
   Foundational            Pathophysiology &         Field Triage &
   Systems Architecture    System Fault Trees        Runtime Debugging
   "Know the spec sheet"   "Read the crash logs"     "Debug it live"
        ~36 h                   ~48 h                     ~30 h
```

**Total estimated study load: ~114 hours.**

---

### 🟢 Phase 1 — Foundational Systems Architecture

> _Healthy operating parameters and the tissue-level production plants. You cannot detect a fault without first knowing the spec sheet._

| Module | Focus | Key Bilingual Terms | Hours |
| :--- | :--- | :--- | :---: |
| **1.1** | The Hardware Stack Overview — body-system block diagram | — | **6** |
| **1.2** | Cellular Production Plants: **Bone Marrow** | نخاع العظم | **8** |
| **1.3** | The Lymphatic Transit Network | الجهاز اللمفاوي | **8** |
| **1.4** | Localized Filter Checkpoints: **Lymph Nodes** | عقدة ليمفاوية | **6** |
| **1.5** | Healthy Operating Parameters (HR, RR, Temp, CRT, MM color) | المؤشرات الحيوية | **8** |
| | | **Phase Subtotal** | **36** |

**Exit criterion:** You can recite normal feline/canine baselines from memory and explain *where* each blood cell line is manufactured and filtered.

---

### 🟠 Phase 2 — Pathophysiology & System Fault Trees

> _How viral, bacterial, and toxic payloads execute code-injection attacks — and how a single breach cascades into total system failure._

| Module | Focus | Key Bilingual Terms | Hours |
| :--- | :--- | :--- | :---: |
| **2.1** | Threat Model: Viral · Bacterial · Toxic payload classes | مُمْرِض / السموم | **8** |
| **2.2** | Code-Injection Mechanics: how pathogens hijack host cells | العدوى الفيروسية | **10** |
| **2.3** | **Immune Wipe:** Feline Panleukopenia | طاعون القطط الفيروسي | **12** |
| **2.4** | Gut Barrier Breach & Bacterial Translocation | حاجز الأمعاء | **8** |
| **2.5** | Cascade Failure: Systemic Sepsis & Liver Shutdown | الإنتان / فشل الكبد | **10** |
| | | **Phase Subtotal** | **48** |

**Exit criterion:** You can trace any presenting symptom *backward* to its originating subsystem fault, and *forward* to its downstream cascade.

---

### 🔴 Phase 3 — Field Triage & Runtime Debugging

> _A deterministic, step-by-step diagnostic loop for rescuers facing acute system failure — executed before professional veterinary handoff._

| Module | Focus | Key Bilingual Terms | Hours |
| :--- | :--- | :--- | :---: |
| **3.1** | The Deterministic Triage Loop (master control flow) | الفرز الميداني | **4** |
| **3.2** | **A/B** — Airway & Breathing subsystem check | مجرى الهواء / التنفس | **6** |
| **3.3** | Thermal Defense — hypo/hyperthermia management | الحرارة / انخفاض الحرارة | **6** |
| **3.4** | Perfusion Debug — **Capillary Refill Time** via gum barriers | زمن امتلاء الشعيرات | **6** |
| **3.5** | Fluid Collapse & Shock Management → Pro Handoff | الصدمة / نقص السوائل | **8** |
| | | **Phase Subtotal** | **30** |

**Exit criterion:** Under time pressure, you can run the full triage loop on a collapsed animal and produce a clean, structured handoff report for the receiving veterinarian.

---

## 🧯 Phase 2 Fault Trees — ASCII Block Diagrams

These are the core debugging artifacts of Phase 2. **Read top-to-bottom: ingress → target → local fault → systemic cascade.** Arabic terminology is mapped in the **TERM MAP** beneath each diagram (kept outside the boxes to preserve monospace alignment).

### Fault Tree A — Feline Panleukopenia: The Immune-Wipe Cascade

```text
                        +==============================+
                        |   PATHOGEN PAYLOAD INGRESS   |
                        |   FPV  (fecal-oral vector)   |
                        +===============+==============+
                                        |
                                        v
                        +------------------------------+
                        |  TARGET: HIGH-MITOSIS CORES  |
                        |  (rapidly dividing cells)    |
                        +------------------------------+
                 +----------------------+----------------------+
                 v                      v                      v
        +-----------------+   +-----------------+   +-----------------+
        |  BONE MARROW    |   |  GUT CRYPT ROW  |   | LYMPHOID TISSUE |
        |  WBC factory    |   |  barrier line   |   |  immune nodes   |
        |  >> OFFLINE     |   |  >> BREACHED    |   |  >> DEPLETED    |
        +--------+--------+   +--------+--------+   +--------+--------+
                 |                     |                     |
                 v                     v                     v
        +-----------------+   +-----------------+   +-----------------+
        | PANLEUKOPENIA   |   | BACTERIAL       |   | FIREWALL DOWN   |
        | WBC count -> 0  |   | TRANSLOCATION   |   | no AB response  |
        +--------+--------+   +--------+--------+   +--------+--------+
                 +---------------------+---------------------+
                                       |
                                       v
                        +------------------------------+
                        |    SYSTEMIC SEPSIS CASCADE    |
                        |   (uncontrolled infection)    |
                        +===============+==============+
                                        |
                                        v
                        +------------------------------+
                        |  MULTI-ORGAN FAULT / SHOCK   |
                        |  liver shutdown . DIC . death|
                        +------------------------------+
```

**TERM MAP (EN ⇄ AR):**

| Node | English | Arabic |
| :--- | :--- | :--- |
| Ingress | Feline Panleukopenia Virus (FPV) | طاعون القطط الفيروسي |
| Target | Bone marrow (WBC factory) | نخاع العظم |
| Target | Lymphoid tissue (immune nodes) | الجهاز اللمفاوي / عقدة ليمفاوية |
| Local fault | Panleukopenia (collapse of all white cell lines) | نقص الكريات البيض الشامل |
| Local fault | Gut barrier breach | حاجز الأمعاء |
| Cascade | Systemic sepsis | الإنتان الجهازي |
| Cascade | Liver shutdown | فشل الكبد |

---

### Fault Tree B — The Three Payload Classes (Threat Model)

```text
     VIRAL payload          BACTERIAL payload         TOXIC payload
   (code injection)        (resource hijack)        (corrosive input)
          |                        |                        |
          v                        v                        v
   hijacks the host         releases endo- and        direct damage to
   cell's replication       exo-toxins; consumes      cell membranes and
   machinery to clone       host nutrients and        enzyme systems
   itself                   oxygen                    (no replication)
          |                        |                        |
          +------------------------+------------------------+
                                   |
                                   v
                    +---------------------------------+
                    |   CELLULAR DEGRADATION / DEATH  |
                    |        (necrosis | apoptosis)   |
                    +----------------+----------------+
                                     |
                                     v
                    +---------------------------------+
                    |  INFLAMMATORY RESPONSE OVERLOAD |
                    |   (the firewall over-triggers)  |
                    +---------------------------------+
```

**TERM MAP (EN ⇄ AR):**

| Class | English | Arabic |
| :--- | :--- | :--- |
| Vector 1 | Viral payload (code injection) | العدوى الفيروسية |
| Vector 2 | Bacterial payload (resource hijack) | العدوى البكتيرية |
| Vector 3 | Toxic payload (corrosive input) | السموم |
| Convergence | Cellular degradation / necrosis | موت الخلايا |
| Output | Inflammatory overload | الاستجابة الالتهابية |

---

## 🧪 Phase 3 Preview — The Deterministic Triage Loop

The full loop ships in `workspace/TRIAGE_SLIDES.md`. The control-flow contract is:

```text
   START
     |
     v
   [ A ] AIRWAY clear?  --no--> clear obstruction --> re-check
     | yes
     v
   [ B ] BREATHING present & effective?  --no--> support / escalate
     | yes
     v
   [ T ] TEMPERATURE in range?  --no--> warm (hypo) / cool (hyper)
     | yes
     v
   [ C ] CRT < 2s & gums pink?  --no--> treat for shock / poor perfusion
     | yes
     v
   [ F ] FLUID status stable?  --no--> manage collapse, keep warm
     | yes
     v
   >>> STRUCTURED HANDOFF TO VETERINARIAN <<<
```

> Every branch — **without exception** — converges on professional veterinary handoff. The loop's job is to **buy time**, not to cure.

---

## 🗂️ Repository Architecture

The blueprint spans **three delivery tiers** so that the same curriculum can be consumed as code, as a workspace, or as academic literature.

```text
project-kumquat/
│
├── README.md                     # ◀ YOU ARE HERE — the core interface
├── ROADMAP.md                    # Visualization AST (Markmap.js / roadmap.sh)
│
├── data/
│   └── CURRICULUM_MATRIX.json     # Machine-readable curriculum (LMS import)
│
├── workspace/
│   ├── NOTION_LAYOUT.md           # Notion database + Kanban blueprint
│   └── TRIAGE_SLIDES.md           # Marp field-deployment slide deck
│
└── academic/
    └── THESIS_TEMPLATE.tex        # University-grade LaTeX thesis (XeLaTeX)
```

| Tier | Format | Files | Built for |
| :--- | :--- | :--- | :--- |
| **1 · Open-Source Code Repository** | Markdown & JSON | `README.md`, `ROADMAP.md`, `CURRICULUM_MATRIX.json` | GitHub, scrapers, LMS importers |
| **2 · Interactive Digital Workspace** | Notion schema & Markdown slides | `NOTION_LAYOUT.md`, `TRIAGE_SLIDES.md` | Self-study tracking, field use on phone/tablet |
| **3 · Academic Research** | LaTeX | `THESIS_TEMPLATE.tex` | Citable, print-ready documentation |

> **Build status of this repo:** `README.md` ✅ · `THESIS_TEMPLATE.tex` ✅ · remaining assets pending review checkpoint.

---

## 🚀 How to Use This Roadmap

1. **Orient** — read this README end-to-end and internalize the *Biology-as-a-Hardware-Stack* mapping.
2. **Plan** — import `data/CURRICULUM_MATRIX.json` into your LMS, or clone the tracker from `workspace/NOTION_LAYOUT.md`.
3. **Visualize** — render `ROADMAP.md` with [Markmap.js](https://markmap.js.org/) or a roadmap.sh custom layout for a node map.
4. **Study** — work Phase 1 → 2 → 3 in order; do not skip the spec sheet.
5. **Deploy** — keep `workspace/TRIAGE_SLIDES.md` (Marp) on your phone for field reference.
6. **Cite** — compile `academic/THESIS_TEMPLATE.tex` with XeLaTeX for a print-ready, Arabic-capable document.

---

## ⚖️ License & Citation

Released under **Creative Commons Attribution–ShareAlike 4.0 (CC-BY-SA-4.0)**. Use it, fork it, translate it, teach with it — keep it open, and keep the attribution.

```bibtex
@misc{project_kumquat,
  title  = {The Engineer's Blueprint for Veterinary Medicine \& Stray Triage},
  author = {Project Kumquat Contributors},
  note   = {Codename Kumquat. Vet-level grounding for non-vets.},
  year   = {2026},
  howpublished = {Open-source education roadmap}
}
```

---

<div align="center">

### 🍊 _When a system goes down, we do not guess — we debug._

**Project Kumquat** · in memory of **Koki**

⚠️ **This is an educational framework, not a veterinary license. Stabilize, then hand off to a professional.**

</div>
