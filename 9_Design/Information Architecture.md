# Information Architecture

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Site Map

```
┌──────────────────────────────────────────────────────────────────────┐
│                        LANDING / HOME                                │
│  ┌────────────────────────────────────────────────────────┐          │
│  │  • Certification selection (if first visit)            │          │
│  │  • Knowledge map (if returning user)                   │          │
│  │  • Continue where you left off (if session exists)     │          │
│  └────────────────────────────────────────────────────────┘          │
└────────────────────────────────┬─────────────────────────────────────┘
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
        ▼                        ▼                        ▼
┌───────────────────┐  ┌───────────────────┐  ┌───────────────────┐
│   KNOWLEDGE MAP    │  │    TOPIC VIEW     │  │   PROGRESS        │
│                    │  │                   │  │   DASHBOARD       │
│ • Module list      │  │ • Topic title     │  │                   │
│   (expandable)     │  │ • Content body    │  │ • Overall %       │
│ • Weighting %      │  │ • Source citation │  │ • Module progress │
│ • Progress dots    │  │ • Quick Look bar  │  │ • Weak topics     │
│ • Search bar       │  │   (related topics)│  │ • Session history │
│   (global)         │  │ • Mark reviewed   │  │ • Practice CTA    │
│                    │  │ • Practice CTA    │  │                   │
└───────────────────┘  └───────────────────┘  └───────────────────┘
        │                        │                        │
        │                        │                        │
        ▼                        ▼                        │
┌───────────────────┐  ┌───────────────────┐              │
│   QUICK LOOK      │  │   PRACTICE QUIZ   │              │
│   (Popover)       │  │                   │              │
│                    │  │ • Question card   │◄────────────┘
│ • Topic summary   │  │ • Answer options  │
│ • "View Full" CTA │  │ • Submit button   │
│ • "Close" CTA     │  │ • Result + expl.  │
│                    │  │ • Progress bar    │
└───────────────────┘  └───────────────────┘
                                │
                                ▼
                       ┌───────────────────┐
                       │   QUIZ RESULTS    │
                       │                   │
                       │ • Score overview  │
                       │ • Topic breakdown │
                       │ • Weak topic list │
                       │ • Retake CTA      │
                       │ • Return to map   │
                       └───────────────────┘
```

---

## Page Inventory

| # | Page | Purpose | Entry Point | Priority |
|---|------|---------|-------------|----------|
| P01 | Certification Selection | First-time landing: choose which certification to study | App launch | High |
| P02 | Knowledge Map | Main navigation hub; shows syllabus structure with progress | Post-selection; global nav | High |
| P03 | Topic Content | Full content view for a single syllabus topic | Click from map, search result, or Quick Look | High |
| P04 | Quick Look (Popover) | Preview a topic without leaving current page | Hover/tap on topic link | High |
| P05 | Practice Quiz | Interactive quiz for a module or weak topic set | "Practice" CTA | High |
| P06 | Quiz Results | Score and weak topic identification after quiz | After quiz completion | High |
| P07 | Progress Dashboard | Comprehensive view of all progress data | Global nav | Medium |
| P08 | Search Results | List of topics matching search query | Search bar input | High |

---

## Navigation Structure

### Global Navigation (visible on all pages)

| Element | Destination | Notes |
|---------|-------------|-------|
| Logo / Brand | Home (Knowledge Map) | Always visible |
| Search Bar | Inline search → P08 | Always visible |
| Progress Indicator | P07 (Dashboard) | Shows % complete |
| Certification Name | P01 (Switch cert) | Dropdown for future multi-cert |

### Page-level Navigation

| Page | Primary Action | Secondary Actions |
|------|---------------|------------------|
| P01 (Selection) | Choose certification | None |
| P02 (Map) | Expand module / click topic | Search, Progress Dashboard |
| P03 (Topic) | Read content / Mark reviewed | Practice CTA, Back to Map |
| P04 (Quick Look) | View summary / Click "Full Content" | Close popover |
| P05 (Quiz) | Answer question / Submit | Progress bar |
| P06 (Results) | Review / Retake / Return | Navigate to weak topics |
| P07 (Dashboard) | Review progress | Click weak topic → P03 |

---

## Content Hierarchy (per Topic)

```
Topic
├── Topic Name (as defined in official syllabus)
├── Parent Module Name
├── Content Body
│   ├── Core concept explanation
│   ├── Key terminology
│   └── Important distinctions / edge cases
├── Source Citation
│   ├── Document title
│   └── Link to official Microsoft docs
└── Related Topics (links to Quick Look)
```

---

## Labeling Convention

Labels should match **official Microsoft syllabus terminology** exactly. This ensures:

1. Users who studied the official syllabus recognize the structure immediately
2. Search works correctly (terms match what users type)
3. Future integration with Microsoft content is simpler

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | For MVP, only one certification (AI-901) will be available — P01 is a simple landing page rather than a full selection UI |
| 2 | Search bar is persistent across all pages — users should never have to navigate to search |
| 3 | Quick Look is a non-modal popover (can be dismissed by clicking outside) |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | Keep the IA flat — no page should be more than 3 clicks away from any other page |
| 2 | The Knowledge Map (P02) should be the default landing for returning users, not the Certification Selection (P01) |
| 3 | In interviews, explain the IA decision: "Mirroring the official syllabus structure minimizes cognitive load for users who already understand the exam framework" |
