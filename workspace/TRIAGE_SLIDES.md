---
marp: true
title: Project Kumquat — Field Triage Deck
author: Project Kumquat
paginate: true
theme: default
backgroundColor: "#FBFBFD"
color: "#14202B"
style: |
  section {
    font-size: 30px;
    padding: 44px 56px;
    font-family: -apple-system, "Segoe UI", Roboto, sans-serif;
  }
  h1 { color: #0B3D5C; font-size: 1.5em; line-height: 1.12; }
  h2 { color: #0B3D5C; font-size: 1.18em; }
  strong { color: #0B3D5C; }
  em { color: #5B6770; font-style: normal; font-weight: 600; }
  blockquote { font-size: 0.92em; color: #5B6770; border-left: 6px solid #E08A2B; }
  table { font-size: 1.05em; }
  section.lead { text-align: center; }
  section.A { border-top: 18px solid #2E7D32; }
  section.B { border-top: 18px solid #1565C0; }
  section.T { border-top: 18px solid #E08A2B; }
  section.C { border-top: 18px solid #6A1B9A; }
  section.F { border-top: 18px solid #B00020; }
---

<!-- _class: lead -->

# 🐾 FIELD TRIAGE

## Project Kumquat · Runtime Debugging

**Stabilize → Document → Hand off.**

*الفرز الميداني*

> Swipe through the loop. Big text = read it standing over the animal.

---

<!-- _class: lead -->

# ⚠️ READ FIRST

This deck **does not** replace a veterinarian.

It buys **time** and produces **data**.

Every path ends the same way:

## → Hand off to a professional vet.

*التحويل للطبيب البيطري*

---

# 🔁 THE LOOP

Run **in order**. Each step gates the next.

## A → B → T → C → F

- 🟢 **A** — Airway · *مجرى الهواء*
- 🔵 **B** — Breathing · *التنفس*
- 🟠 **T** — Temperature · *الحرارة*
- 🟣 **C** — Circulation / CRT · *التروية*
- 🔴 **F** — Fluid status · *السوائل*

**Do not jump ahead.**

---

# 📋 SPEC SHEET — Normal (Cat)

Know the baseline before you call a fault.

| Read | Normal |
| :-- | :-- |
| 🌡️ **Temp** | 38.1–39.2 °C |
| ❤️ **Heart rate** | 140–220 / min |
| 🫁 **Breaths** | 20–30 / min |
| ⏱️ **CRT** | **under 2 sec** |
| 👄 **Gums** | **pink + moist** |

> Kittens chill fast. A cold kitten is already out of spec.

---

<!-- _class: A -->

# 🟢 STEP A — AIRWAY

*مجرى الهواء*

## Is the airway **clear**?

- Look in the mouth — fluid, debris, tongue position
- Clear **visible** obstruction only — gently
- Re-check after clearing

✅ **CLEAR** → go to **B**
⚠️ **BLOCKED** → clear it, then re-check

---

<!-- _class: B -->

# 🔵 STEP B — BREATHING

*التنفس*

## Present **and** effective?

- Watch the chest rise — count 15 sec ×4
- Effort, noise, or **blue gums** = trouble
- Open airway · keep neck straight · escalate

✅ **BREATHING** → go to **T**
⚠️ **NOT EFFECTIVE** → support + **escalate NOW**

---

<!-- _class: T -->

# 🟠 STEP T — TEMPERATURE

*الحرارة*

## In range (38.1–39.2 °C)?

- **Too LOW** (common in collapse):
  - Warm **gradually** — towels, body heat
  - 🚫 No sudden / aggressive heat
  - 🚫 Do **not** feed a cold, shut-down animal
- **Too HIGH:** cool gently, shade, airflow

✅ **IN RANGE** → go to **C**

---

<!-- _class: C -->

# 🟣 STEP C — CRT + GUMS

*زمن امتلاء الشعيرات الدموية*

## Press gum → release → **count seconds**

- **Pink + under 2 sec** = perfusion OK
- **Over 2 sec / pale** = poor perfusion → shock path

The gum is your **status LED**.

✅ **under 2 s + PINK** → go to **F**
⚠️ **over 2 s / PALE** → treat for shock

---

<!-- _class: C -->

# 👄 GUM COLOR DECODER

- 🩷 **Pink** — nominal
- ⚪ **Pale / white** — shock · anemia · poor perfusion
- 🔵 **Blue** — oxygen failure → **escalate now**
- 🧱 **Brick red** — hyperdynamic **sepsis**
- 🟡 **Yellow** — liver / red-cell breakdown

> Color **+** CRT together tell you which system is failing.

---

<!-- _class: F -->

# 🔴 STEP F — FLUID / SHOCK

*الصدمة · السوائل*

## Stable, or collapsing?

- Collapse signs: weak pulse, cold limbs, pale gums, sunken eyes
- **Keep warm**, minimize handling
- Prevent further loss · prepare transport
- IV fluids are a **vet** intervention — get there fast

⚠️ **COLLAPSE** → stabilize + **transport immediately**

---

<!-- _class: F -->

# 🧮 FLUID DEFICIT (for the vet)

Hand them a **number**, not a guess.

## deficit (mL) = BW(kg) × D(%) × 10

- **BW** = body weight in kg
- **D** = estimated dehydration %

**Shock index = HR ÷ SAP** — rising = worse

> Write it on the handoff note. Let the vet dose the fluids.

---

# ✅ HANDOFF REPORT

Read this out to the receiving vet:

- ⏱️ **Time** found + time on scene
- 📋 **Baselines:** Temp · HR · RR · CRT · gum color
- 🔻 **Deviations** from normal
- 🧰 **Interventions:** warming, airway, position
- 🧮 **Computed deficit** (if estimated)
- 🐱 **History:** age, environment, exposure

**Stabilize · Document · Hand off.**

---

# 🚨 ESCALATE-NOW FLAGS

Do not finish the loop — **move** if you see:

- 🔵 **Blue** gums / not breathing
- 🚫 **No pulse** / unresponsive
- ⏱️ **CRT over 3 sec** + pale
- 🩸 Active heavy bleeding
- 🌡️ Severe cold + collapse

> When in doubt: warm, protect the airway, transport.

---

<!-- _class: lead -->

# 🍊 We don't guess. We debug.

**Project Kumquat** · in memory of **Koki**

*طاعون القطط الفيروسي*

> Educational field aid — not a veterinary license.
> Always hand off to a professional veterinarian.
