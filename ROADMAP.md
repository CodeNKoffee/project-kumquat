---
title: Project Kumquat — Roadmap
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 3
  maxWidth: 320
---

<!--
  ROADMAP.md  —  The Visualization AST
  ---------------------------------------------------------------
  This file is a nested, hierarchical outline designed to compile
  directly into an interactive node map.

  • Markmap.js  : paste into https://markmap.js.org/repl  OR run
                  `npx markmap-cli ROADMAP.md` to emit an HTML mind-map.
                  The YAML front-matter above configures the render.
  • roadmap.sh  : the heading + nested-list tree maps onto a custom
                  roadmap layout (Phase = parent node, Module = child
                  node, Milestones/Terms = leaf nodes).

  AST CONTRACT
  ------------
  # H1   → root
  ## H2  → phase node      (also: Orientation, Mastery & Handoff)
  ### H3 → module node      (dotted id, e.g. 2.3)
  - list → leaf nodes       (**Milestones**, **Terms (EN / AR)**)

  NOTE: thematic-break rules (---) are intentionally omitted from the
  body so Markmap parses one clean tree; phase boundaries are encoded
  as H2 nodes, which is what produces visual separation in the map.
-->

# 🐾 Project Kumquat

## 🧭 Orientation

### Core Abstraction — Biology as a Hardware Stack
- **Organs** → specialized sub-routines
- **Vascular network** → fluid plumbing · **الجهاز الدوراني**
- **Immune system** → multi-tier firewall · **الجهاز المناعي**
- **Liver** → detox / waste daemon · **الكبد**
- **Gut barrier** → perimeter I/O wall · **حاجز الأمعاء**
- **Mucous membranes** → status LEDs · **الأغشية المخاطية**

### Guardrail
- **Vet-level grounding for non-vets** — not a DVM substitute
- Every path ends at: **stabilize → document → professional handoff**
- Audience: field rescuers, wildlife responders, bio-engineers

### Study Load
- **Total ≈ 114 hours** → Phase 1 (36h) · Phase 2 (48h) · Phase 3 (30h)

## 🟢 Phase 1 — Foundational Systems Architecture · ~36h
**هندسة الأنظمة الأساسية** — _the specification sheet_

### 1.1 The Hardware Stack Overview · 6h
- **Milestones**
  - Draw a top-level block diagram of organ sub-routines + plumbing
  - Fix the engineering vocabulary used across all phases
  - Define **homeostasis** as the closed-loop control target
- **Terms (EN / AR)**
  - Body systems / **أجهزة الجسم**
  - Anatomy / **التشريح**
  - Physiology / **علم وظائف الأعضاء**
  - Homeostasis / **الاتزان الداخلي**

### 1.2 Cellular Production Plants: Bone Marrow · 8h
- **Milestones**
  - Map the factory output: RBCs, WBCs, platelets
  - Explain why high-mitosis cores are high-value pathogen targets
  - Tie WBC production rate to firewall capacity
- **Terms (EN / AR)**
  - Bone marrow / **نخاع العظم**
  - Hematopoiesis / **تكوين الدم**
  - White blood cells / **خلايا الدم البيضاء**
  - Platelets / **الصفائح الدموية**

### 1.3 The Lymphatic Transit Network · 8h
- **Milestones**
  - Trace one-way lymph flow from interstitium back to circulation
  - Contrast low-pressure return bus vs. pressurized vascular loop
  - Show how immune cells + antigens are routed to checkpoints
- **Terms (EN / AR)**
  - Lymphatic system / **الجهاز اللمفاوي**
  - Lymph / **السائل اللمفاوي**
  - Lymphatic vessels / **الأوعية اللمفاوية**

### 1.4 Localized Filter Checkpoints: Lymph Nodes · 6h
- **Milestones**
  - Locate major node clusters; read a reactive node as a status flag
  - Describe antigen screening + adaptive activation at the node
  - Interpret node enlargement as active threat processing
- **Terms (EN / AR)**
  - Lymph node / **عقدة ليمفاوية**
  - Immune checkpoint / **نقطة تفتيش مناعية**
  - Antigen / **مستضد** · Antibody / **جسم مضاد**

### 1.5 Healthy Operating Parameters · 8h
- **Milestones**
  - Recite feline baselines from memory: Temp 38.1–39.2°C · HR 140–220 · RR 20–30 · CRT <2s · pink MM
  - Note key canine baseline differences
  - Flag any reading drifting out of spec
- **Terms (EN / AR)**
  - Vital signs / **العلامات الحيوية**
  - Heart rate / **معدل ضربات القلب**
  - Capillary refill time / **زمن امتلاء الشعيرات الدموية**
  - Mucous membranes / **الأغشية المخاطية**

## 🟠 Phase 2 — Pathophysiology & System Fault Trees · ~48h
**الفيزيولوجيا المرضية وأشجار أعطال النظام** — _reading the crash logs_

### 2.1 Threat Model: Viral · Bacterial · Toxic Payloads · 8h
- **Milestones**
  - Classify any insult into one of three payload classes
  - Match each class to its damage signature
  - Explain replication (viral) vs. non-replication (toxic)
- **Terms (EN / AR)**
  - Pathogen / **العامل الممرض**
  - Virus / **فيروس** · Bacteria / **بكتيريا**
  - Toxin / **السموم**

### 2.2 Code-Injection Mechanics · 10h
- **Milestones**
  - Walk the bind → inject → redirect → rupture cycle
  - Explain targeting of high-mitosis cores
  - Connect mechanics to the Phase 1 plants at risk
- **Terms (EN / AR)**
  - Viral infection / **العدوى الفيروسية**
  - Viral replication / **التكاثر الفيروسي**
  - Host cell / **الخلية المضيفة**

### 2.3 Immune Wipe: Feline Panleukopenia · 12h
- **Milestones**
  - Explain simultaneous strike on marrow + crypts + lymphoid tissue
  - Define **panleukopenia** as collapse of all white-cell lines
  - Summarize prevention via core vaccination
- **Terms (EN / AR)**
  - Feline panleukopenia / **طاعون القطط الفيروسي**
  - Feline parvovirus / **الفيروس الصغير السنوري**
  - Total leukopenia / **نقص الكريات البيض الشامل**
  - Vaccination / **التطعيم**

### 2.4 Gut-Barrier Breach & Bacterial Translocation · 8h
- **Milestones**
  - Explain loss of crypt cells → perimeter wall breach
  - Describe bacterial translocation while the firewall is down
  - Link gut failure to systemic infection
- **Terms (EN / AR)**
  - Intestinal barrier / **حاجز الأمعاء**
  - Bacterial translocation / **انتقال البكتيريا**
  - Enteritis / **التهاب الأمعاء** · Diarrhea / **الإسهال**

### 2.5 Cascade Failure: Sepsis & Liver Shutdown · 10h
- **Milestones**
  - Trace translocation → systemic sepsis → distributive shock
  - Explain endotoxin overload + liver daemon shutdown
  - Describe DIC as consumption of the platelet subsystem
- **Terms (EN / AR)**
  - Sepsis / **الإنتان** · Septic shock / **الصدمة الإنتانية**
  - Liver failure / **فشل الكبد**
  - DIC / **التخثر المنتشر داخل الأوعية**

## 🔴 Phase 3 — Field Triage & Runtime Debugging · ~30h
**الفرز الميداني وتصحيح الأخطاء أثناء التشغيل** — _debug it live_

### 3.1 The Deterministic Triage Loop · 4h
- **Milestones**
  - Execute **A → B → T → C → F** in strict order
  - Explain why each check gates the next
  - State the single exit: clean veterinary handoff
- **Terms (EN / AR)**
  - Triage / **الفرز** · Field triage / **الفرز الميداني**
  - Emergency assessment / **التقييم الطارئ**
  - Veterinary handoff / **التحويل للطبيب البيطري**

### 3.2 Airway & Breathing Subsystem Check · 6h
- **Milestones**
  - Assess airway patency; clear visible obstruction safely
  - Judge effective breathing; know the escalation trigger
  - Recognize cyanosis as an oxygenation-failure flag
- **Terms (EN / AR)**
  - Airway / **مجرى الهواء** · Breathing / **التنفس**
  - Respiratory distress / **ضائقة تنفسية**
  - Cyanosis / **الزُّراق**

### 3.3 Thermal Defense · 6h
- **Milestones**
  - Recognize hypothermia as the common collapsed-kitten state
  - Apply gradual warming; avoid aggressive re-warming faults
  - Withhold feeding from a hypothermic, shut-down gut
- **Terms (EN / AR)**
  - Body temperature / **درجة حرارة الجسم**
  - Hypothermia / **انخفاض حرارة الجسم**
  - Hyperthermia / **فرط الحرارة**

### 3.4 Perfusion Debug: Capillary Refill Time · 6h
- **Milestones**
  - Perform the gum blanch test; time refill vs. <2s baseline
  - Map MM color → interpretation (pale · blue · brick-red · yellow)
  - Decide when poor perfusion mandates shock management
- **Terms (EN / AR)**
  - Capillary refill time / **زمن امتلاء الشعيرات الدموية**
  - Perfusion / **التروية**
  - Gums / **اللثة** · MM color / **لون الأغشية المخاطية**

### 3.5 Fluid Collapse & Shock → Handoff · 8h
- **Milestones**
  - Estimate dehydration %, compute fluid deficit = BW(kg) × D(%) × 10
  - Manage shock; conserve heat; prevent further loss
  - Produce structured handoff: baselines · deviations · interventions · deficit
- **Terms (EN / AR)**
  - Shock / **الصدمة** · Hypovolemia / **نقص حجم الدم**
  - Dehydration / **الجفاف**
  - Fluid therapy / **العلاج بالسوائل**

## 🎓 Mastery & Handoff

### Exit Criteria
- **Phase 1** — recite baselines; locate every production + filter site
- **Phase 2** — trace any symptom backward to fault + forward to cascade
- **Phase 3** — run the full loop under pressure; deliver a clean handoff

### The One-Line Contract
- _When a system goes down, we do not guess — we debug._
- In memory of **Koki** 🍊 · **طاعون القطط الفيروسي**
