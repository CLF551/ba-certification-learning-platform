# AS-IS Process: Current Certification Study Workflow

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Based on first-hand experience |

## Process Owner

Project Initiator (self-taught certification candidate)

---

## Process Flow

```
┌─────────────────────────────────────────────────────────┐
│  STEP 1: Discovery                                      │
│  ┌─────────────────────────────────────┐                │
│  │ "What is this certificate?"         │                │
│  │ "Who provides it?"                  │                │
│  │ "Does it cost money?"               │                │
│  │ "Self-study or paid course?"        │                │
│  └──────────────┬──────────────────────┘                │
│                 ▼                                       │
│  ┌─────────────────────────────────────┐                │
│  │ Search Google / Microsoft website   │                │
│  └──────────────┬──────────────────────┘                │
└─────────────────┬───────────────────────────────────────┘
                  ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 2: Locate Official Learning Path                  │
│  ┌─────────────────────────────────────┐                │
│  │ Open Microsoft Learn                │                │
│  │ Navigate to AI-901 certification    │                │
│  │ Confirm the official syllabus       │                │
│  └──────────────┬──────────────────────┘                │
└─────────────────┬───────────────────────────────────────┘
                  ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 3: Sequential Study                               │
│  ┌─────────────────────────────────────┐                │
│  │ Start from Module 1                 │                │
│  │ Read through each topic page        │                │
│  │ Follow Microsoft Learn's content    │                │
│  │ order                               │                │
│  └──────────────┬──────────────────────┘                │
└─────────────────┬───────────────────────────────────────┘
                  ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 4: Knowledge Gap Encountered                      │
│  ┌─────────────────────────────────────┐                │
│  │ Hit an unfamiliar concept or term   │                │
│  │                                     │                │
│  │ ┌── Is it clear from context? ─┐    │                │
│  │ │  YES → Continue reading      │    │                │
│  │ │  NO → Go to Step 5           │    │                │
│  │ └──────────────────────────────┘    │                │
│  └──────────────┬──────────────────────┘                │
└─────────────────┬───────────────────────────────────────┘
                  ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 5: Use External Tools                             │
│  ┌─────────────────────────────────────┐                │
│  │ Open AI tool (ChatGPT / Claude /    │                │
│  │ NotebookLM)                         │                │
│  │                                     │                │
│  │ ┌── Is the answer trustworthy? ──┐  │                │
│  │ │  YES → Accept and continue     │  │                │
│  │ │  NO → Open translation tool;   │  │                │
│  │ │       manually search official │  │                │
│  │ │       docs for verification    │  │                │
│  │ └────────────────────────────────┘  │                │
│  │                                     │                │
│  │ Result: Content learned but with    │                │
│  │ uncertainty and context switching   │                │
│  └──────────────┬──────────────────────┘                │
└─────────────────┬───────────────────────────────────────┘
                  ▼
┌─────────────────────────────────────────────────────────┐
│  STEP 6: Continue or Abandon                            │
│  ┌─────────────────────────────────────┐                │
│  │ Return to Microsoft Learn           │                │
│  │ Continue sequential reading         │                │
│  │ OR                                  │                │
│  │ Stop due to accumulated friction    │                │
│  └─────────────────────────────────────┘                │
└─────────────────────────────────────────────────────────┘
```

---

## Pain Points Identified

| Step | Pain Point | Impact |
|------|------------|--------|
| 1 (Discovery) | Multiple unorganized searches; no single source of truth for certification info | Time wasted before learning even starts |
| 2 (Locate) | Manual navigation through Microsoft Learn | Friction before the first study session |
| 3 (Study) | Passive reading — no interaction, no progress granularity | Low engagement |
| 4 (Gap) | No immediate help within the learning environment | Learning flow interrupted |
| 5 (External Tools) | Context switching: Learn → AI → Translate → Learn | Cognitive load increases; time wasted |
| 5 (External Tools) | AI answers may not align with syllabus | User uncertainty |
| 5 (External Tools) | Verification requires manual search across multiple official pages | High friction → may skip verification |
| 6 (Continue) | Accumulated fatigue from context switching | Risk of abandoning study session |

---

## Quantitative Summary

| Metric | Estimate |
|--------|----------|
| Tools used per study session | 2-3 (Microsoft Learn + AI + possibly translation) |
| Context switches per knowledge gap | 2-3 (Learn → AI → verify → Learn) |
| Time per unresolved gap | 5-15 minutes (if verified) |
| Time per skipped gap | 0 minutes (but knowledge remains fuzzy) |
| Estimated frustration rate | High for gaps requiring verification |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | This AS-IS process represents one learner's workflow; other candidates may differ |
| 2 | The process is described for self-study candidates (not classroom-based) |
| 3 | "Context switching" is the primary source of friction, not content difficulty |
