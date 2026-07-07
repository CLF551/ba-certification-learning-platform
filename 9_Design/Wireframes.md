# Wireframes

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Text + ASCII wireframes; ready for Draw.io translation |

## Design Principles

- **Mobile-first**: Layout designed for small screen first, then scales up
- **Minimal taps**: Any action within 3 taps from any screen
- **Content-focused**: No decorative elements; every pixel serves a purpose

---

## W01: Certification Selection (First Visit)

### Description

The first screen a new user sees. Clean, minimal. The purpose is to make one decision: "Which certification do you want to study?"

Currently only AI-901 is available, but the layout is designed for future expansion.

### Desktop Layout

```
┌────────────────────────────────────────────────────────────┐
│                                                            │
│                    Learn Smarter                           │
│           AI-powered certification coaching                │
│                                                            │
│  ┌────────────────────────────────────────────────────┐   │
│  │                                                    │   │
│  │   ┌──────────────────────────────────┐             │   │
│  │   │  Microsoft Azure AI Fundamentals │             │   │
│  │   │         (AI-901)                 │             │   │
│  │   │     [  Start Learning  ]         │             │   │
│  │   └──────────────────────────────────┘             │   │
│  │                                                    │   │
│  │   ┌──────────────────────────────────┐             │   │
│  │   │        More certifications      │             │   │
│  │   │            Coming Soon          │             │   │
│  │   └──────────────────────────────────┘             │   │
│  │                                                    │   │
│  └────────────────────────────────────────────────────┘   │
│                                                            │
│              [Built on official syllabus]                  │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Mobile Layout

```
┌────────────────────────────┐
│                            │
│     Learn Smarter          │
│  AI-powered coaching       │
│                            │
│  ┌──────────────────────┐  │
│  │                      │  │
│  │   Azure AI Fund.     │  │
│  │      (AI-901)        │  │
│  │                      │  │
│  │  [ Start Learning ]  │  │
│  │                      │  │
│  └──────────────────────┘  │
│                            │
│  ┌──────────────────────┐  │
│  │  More: Coming Soon   │  │
│  └──────────────────────┘  │
│                            │
│  Built on official syllabus│
└────────────────────────────┘
```

### Interactive Notes

| Element | Behavior |
|---------|----------|
| "Start Learning" button | Tap → Navigate to Knowledge Map (W02) |
| "Coming Soon" card | Tap → No action; visual placeholder only |
| Footer text | Static; builds trust |

---

## W02: Knowledge Map (Main Navigation Hub)

### Description

The **core screen** of the platform. This is where users spend most of their time.

Shows the full AI-901 syllabus as an expandable tree. Each module shows its exam weight, and each topic shows a read status indicator.

### Desktop Layout

```
┌────────────────────────────────────────────────────────────┐
│ [Logo]  [🔍 Search...                  ]   [45%] [≡]      │
├────────────────────────────────────────────────────────────┤
│                                                            │
│  AI-901: Microsoft Azure AI Fundamentals                   │
│                                                            │
│  ┌──────────────────────────────────────────────────┐      │
│  │ ▶ Module 1: Describe AI workloads (20-25%)       │      │
│  │    ○ Identify AI workloads                    ✅  │      │
│  │    ○ Identify Azure AI services               ✅  │      │
│  │    ○ Identify generative AI workloads         ⬜  │      │
│  └──────────────────────────────────────────────────┘      │
│                                                            │
│  ┌──────────────────────────────────────────────────┐      │
│  │ ▶ Module 2: Azure AI Services (25-30%)           │      │
│  │    ○ Azure Cognitive Services                   ✅  │      │
│  │    ○ Azure Bot Service                          ⬜  │      │
│  │    ○ Azure...                                   ⬜  │      │
│  └──────────────────────────────────────────────────┘      │
│                                                            │
│  ┌──────────────────────────────────────────────────┐      │
│  │ ▶ Module 3: Generative AI (20-25%)               │      │
│  │    (collapsed — 4 topics)                       ✅  │      │
│  └──────────────────────────────────────────────────┘      │
│                                                            │
│  ┌──────────────────────────────────────────────────┐      │
│  │ ▶ Module 4: Computer Vision (15-20%)             │      │
│  │    (collapsed — 3 topics)                       ⬜  │      │
│  └──────────────────────────────────────────────────┘      │
│                                                            │
│  ┌──────────────────────────────────────────────────┐      │
│  │ ▶ Module 5: NLP (15-20%)                         │      │
│  │    (collapsed — 3 topics)                       ⬜  │      │
│  └──────────────────────────────────────────────────┘      │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Mobile Layout

```
┌────────────────────────────┐
│ [Logo] [🔍]    [45%] [≡]  │
├────────────────────────────┤
│ AI-901: Azure AI Fund.     │
│                            │
│ ▶ Module 1: AI workloads   │
│  (20-25%)                  │
│  ○ Identify AI workload ✅ │
│  ○ Identify AI services ✅ │
│  ○ Generative AI ⬜        │
│                            │
│ ▶ Module 2: Azure AI Svc  │
│  (25-30%)                  │
│  ○ Cognitive Services ✅  │
│  ○ Bot Service ⬜          │
│  ○ ... ⬜                   │
│                            │
│ ▶ Module 3: Gen AI (25%) ▶│
│ ▶ Module 4: Comp Vis ▶    │
│ ▶ Module 5: NLP ▶         │
│                            │
└────────────────────────────┘
```

### Legend

| Symbol | Meaning |
|--------|---------|
| ✅ | Topic has been viewed / studied |
| ⬜ | Topic not yet viewed |
| ▶ | Module collapsed (click to expand) |
| ▼ | Module expanded (click to collapse) |
| 🔍 | Search (opens search bar) |
| ≡ | Menu (Progress Dashboard) |

### Interactive Notes

| Element | Behavior |
|---------|----------|
| Module header (▶ Module 1) | Tap → Expand/collapse sub-topics |
| Topic (○ Identify AI workloads) | Tap → Navigate to Topic Content (W03) |
| ✅/⬜ indicator | Read-only; updated when user marks topic as reviewed |
| [45%] badge | Tap → Progress Dashboard (W07) |
| Search icon | Tap → Expand search bar inline |

---

## W03: Topic Content

### Description

Full content view for a single syllabus topic. Shows the official-aligned explanation with source citation. Includes navigation to related topics via Quick Look.

### Desktop Layout

```
┌────────────────────────────────────────────────────────────┐
│ [Logo]  [🔍 Search...                  ]   [45%] [≡]      │
├────────────────────────────────────────────────────────────┤
│  ← Back to Map                                             │
│                                                            │
│  Module 1 > Identify Azure AI workloads                    │
│                                                            │
│  ┌────────────────────────────────────────────────────┐   │
│  │  Azure AI services are cloud-based services        │   │
│  │  designed to help developers build AI-powered      │   │
│  │  applications without requiring deep ML expertise. │   │
│  │                                                    │   │
│  │  Key services include:                             │   │
│  │  • Azure Cognitive Services — pre-built APIs for   │   │
│  │    vision, speech, language, and decision          │   │
│  │  • Azure Machine Learning — build, train, deploy   │   │
│  │  • Azure Bot Service — intelligent bot building    │   │
│  │                                                    │   │
│  │  [Source: Microsoft Learn - AI-901 Module 1]       │   │
│  └────────────────────────────────────────────────────┘   │
│                                                            │
│  Related Topics:                                           │
│  ┌────────────────────────┐  ┌────────────────────────┐   │
│  │  Identify AI workloads │  │  Azure Cognitive        │   │
│  │  [Quick Look 👁]       │  │  Services [Quick Look] │   │
│  └────────────────────────┘  └────────────────────────┘   │
│                                                            │
│  [✅ Mark as Reviewed]    [📝 Practice This Module]        │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Mobile Layout

```
┌────────────────────────────┐
│ [Logo] [🔍]    [45%] [≡]  │
├────────────────────────────┤
│ ← Back                     │
│ Module 1 > Azure AI Svc    │
│                            │
│ ┌────────────────────────┐│
│ │ Azure AI services are  ││
│ │ cloud-based services   ││
│ │ designed to help...    ││
│ │                        ││
│ │ Key services include:  ││
│ │ • Azure Cognitive...   ││
│ │ • Azure Machine...     ││
│ │ • Azure Bot Service   ││
│ │                        ││
│ │ [Source: Microsoft...] ││
│ └────────────────────────┘│
│                            │
│ Related:                   │
│ [Azure Cognitive 👁]      │
│ [AI workloads 👁]         │
│                            │
│ [✅ Mark Reviewed]        │
│ [📝 Practice Module]      │
└────────────────────────────┘
```

### Interactive Notes

| Element | Behavior |
|---------|----------|
| ← Back to Map | Tap → Return to Knowledge Map (W02) |
| Related Topics | Tap "Quick Look 👁" → Show Quick Look popover (W04) |
| Mark as Reviewed | Tap → Toggle to ✅; updates progress on map |
| Practice This Module | Tap → Start Practice Quiz (W05) for this module |

---

## W04: Quick Look Popover

### Description

A lightweight popover that appears on top of the current content. Shows a 1-2 paragraph summary of a related topic. User can either close it or navigate to the full content.

### Desktop/Mobile Layout

```
┌────────────────────────────────────────────────────────────┐
│                                                    [✕]    │
│  ┌──────────────────────────────────────────┐             │
│  │  Quick Look: Azure Cognitive Services    │             │
│  │                                          │             │
│  │  Azure Cognitive Services are cloud-     │             │
│  │  based APIs that enable applications to  │             │
│  │  see, hear, speak, and make decisions.   │             │
│  │  They are categorized into Vision,       │             │
│  │  Speech, Language, and Decision.         │             │
│  │                                          │             │
│  │  [View Full Topic Content →]             │             │
│  └──────────────────────────────────────────┘             │
│                                                            │
│  (Background content dimmed behind popover)                │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Interactive Notes

| Element | Behavior |
|---------|----------|
| [✕] Close | Tap → Close popover; return to background content |
| View Full Topic Content | Tap → Navigate to W03 for the related topic |
| Background overlay | Tap on dimmed area → Also closes popover (non-modal) |

---

## W05: Practice Quiz

### Description

A single-question-per-page quiz interface. Clean, focused. Shows progress through the quiz.

### Desktop/Mobile Layout

```
┌────────────────────────────────────────────────────────────┐
│  ← Back to Module                                          │
│                                                            │
│  Module 1 Practice — Question 3 of 10                      │
│  ████████░░░░░░░░░░░░░░░░░░░░░░░░  30%                     │
│                                                            │
│  ┌────────────────────────────────────────────────────┐   │
│  │                                                    │   │
│  │  Which Azure service provides pre-built APIs for   │   │
│  │  natural language processing?                      │   │
│  │                                                    │   │
│  │  ○  A. Azure Machine Learning                     │   │
│  │  ●  B. Azure Cognitive Services Language           │   │
│  │  ○  C. Azure Bot Service                          │   │
│  │  ○  D. Azure OpenAI Service                       │   │
│  │                                                    │   │
│  │             [  Submit  ]                           │   │
│  └────────────────────────────────────────────────────┘   │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### After Submission (Answer Reveal)

```
┌────────────────────────────────────────────────────────────┐
│  Module 1 Practice — Question 3 of 10                      │
│  ████████░░░░░░░░░░░░░░░░░░░░░░░░  30%                     │
│                                                            │
│  ┌────────────────────────────────────────────────────┐   │
│  │  ✅ Correct!                                       │   │
│  │                                                    │   │
│  │  Azure Cognitive Services Language provides        │   │
│  │  pre-built NLP APIs including sentiment analysis,  │   │
│  │  key phrase extraction, and language detection.    │   │
│  │                                                    │   │
│  │  [Source: AI-901 Module 1 - Azure AI Services]     │   │
│  │                                                    │   │
│  │             [  Next Question →  ]                  │   │
│  └────────────────────────────────────────────────────┘   │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Interactive Notes

| Element | Behavior |
|---------|----------|
| Answer option | Tap → Select (highlighted); tap again → Deselect |
| Submit | Tap → Show answer reveal screen |
| Next Question | Tap → Load next question or navigate to Results (W06) |
| Progress bar | Shows completion %; updates after each question |

---

## W06: Quiz Results

### Description

Shown after quiz completion. Displays overall score, per-topic breakdown, and identified weak topics.

### Desktop Layout

```
┌────────────────────────────────────────────────────────────┐
│  [Logo]  [🔍 Search...                  ]   [45%] [≡]      │
├────────────────────────────────────────────────────────────┤
│  ← Back to Map                                             │
│                                                            │
│  Module 1 Practice — Complete!                             │
│                                                            │
│  ┌────────────────────────────────────────────────────┐   │
│  │                8 / 10  (80%)                        │   │
│  │                                                    │   │
│  │  Score by topic:                                   │   │
│  │  • Identify AI workloads        ✅  2/2  100%      │   │
│  │  • Azure AI services            ⚠️  3/4   75%      │   │
│  │  • Generative AI workloads      ❌  1/3   33%  ◀   │   │
│  └────────────────────────────────────────────────────┘   │
│                                                            │
│  Weak Topics Identified:                                   │
│  ┌──────────────────────────────────────────────────┐     │
│  │  ⚠️ Identify generative AI workloads             │     │
│  │     Score: 33%  [  Review Topic  ]  [  Retry  ]  │     │
│  └──────────────────────────────────────────────────┘     │
│                                                            │
│  [📝 Retake Full Quiz]    [← Back to Knowledge Map]        │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Mobile Layout

```
┌────────────────────────────┐
│ [Logo] [🔍]    [45%] [≡]  │
├────────────────────────────┤
│ ← Back                     │
│                            │
│ Module 1 Practice — Done!  │
│                            │
│ ┌────────────────────────┐│
│ │   8 / 10  (80%)        ││
│ │                        ││
│ │ By topic:              ││
│ │ AI workloads ✅ 100%   ││
│ │ AI services  ⚠️ 75%    ││
│ │ Gen AI ❌ 33% ◀       ││
│ └────────────────────────┘│
│                            │
│ Weak Topics:               │
│ ┌────────────────────────┐│
│ │ Gen AI workloads (33%) ││
│ │ [Review] [Retry]       ││
│ └────────────────────────┘│
│                            │
│ [Retake Quiz] [← Map]     │
└────────────────────────────┘
```

### Interactive Notes

| Element | Behavior |
|---------|----------|
| Review Topic | Tap → Navigate to Topic Content (W03) for that topic |
| Retry | Tap → Start a new quiz focused on that specific topic |
| Retake Full Quiz | Tap → Restart the full module quiz |
| Back to Map | Tap → Return to Knowledge Map (W02) |

---

## W07: Progress Dashboard

### Description

A comprehensive view of the learner's journey. Shows overall progress, weak topics, and activity summary.

### Layout

```
┌────────────────────────────────────────────────────────────┐
│  [Logo]  [🔍 Search...                  ]   [45%] [≡]      │
├────────────────────────────────────────────────────────────┤
│  ← Back                                                    │
│                                                            │
│  Your Progress — AI-901                                    │
│                                                            │
│  ┌────────────────────────────────────────────────────┐   │
│  │  Overall: 45% complete (15 of 33 topics)          │   │
│  │  ████████████████████░░░░░░░░░░░░░░░░░░░ 45%      │   │
│  └────────────────────────────────────────────────────┘   │
│                                                            │
│  Module Progress:                                          │
│  ┌──────────────────────────────────────────────────┐     │
│  │ Module 1: AI workloads        ████████░░░  3/3 ✅ │     │
│  │ Module 2: Azure AI services   ██████░░░░░  4/6    │     │
│  │ Module 3: Generative AI       ██░░░░░░░░░  1/4  ⚠️ │     │
│  │ Module 4: Computer Vision     ░░░░░░░░░░░  0/3    │     │
│  │ Module 5: NLP                 ░░░░░░░░░░░  0/3    │     │
│  └──────────────────────────────────────────────────┘     │
│                                                            │
│  ⚠️ Weak Topics (score < 70%):                             │
│  • Identify Generative AI workloads (33%)                  │
│  • Azure Cognitive Services (60%)                          │
│                                                            │
│  📅 Last studied: Today, 2:30 PM                           │
│  🔥 Study streak: 3 days                                   │
│                                                            │
│  [📝 Practice Weak Topics]  [📖 Continue Studying]         │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

---

## Wireframe Flow Summary

```
W01: Certification Selection
    │
    ▼
W02: Knowledge Map ◄─────────────────────────┐
    │                                        │
    ├──→ W03: Topic Content ──→ W04: Quick   │
    │         │                Look Popover  │
    │         ▼                              │
    │    [Practice CTA]                      │
    │         │                              │
    └──→ W05: Practice Quiz                  │
              │                              │
              ▼                              │
         W06: Quiz Results ──────────────────┘
              │
              ├──→ [Review Topic → W03]
              └──→ [Back to Map → W02]

W07: Progress Dashboard ← accessible from [≡] menu
     ├──→ [Review Topic → W03]
     └──→ [Continue Studying → W02]
```

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | All wireframes assume a web-based responsive design (not native app) |
| 2 | Color coding: ✅ = green, ⚠️ = yellow/orange, ❌ = red, ⬜ = gray |
| 3 | No authentication/login screens needed for MVP |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | Start drawing in Draw.io: begin with W02 (Knowledge Map) — it's the most important and most complex screen |
| 2 | Use W02 → W03 → W05 flow as the "happy path" for user testing |
| 3 | Keep mobile and desktop consistent — only change layout, not content or behavior |
