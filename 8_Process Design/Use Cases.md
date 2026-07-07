# Use Cases

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Use Case Diagram (Text Representation)

```
┌──────────────────────────────────────────────────────┐
│                 Certification Learning Platform       │
│                                                      │
│  ┌──────────┐    ┌───────────────────────┐          │
│  │          │    │ UC-01: View Syllabus  │          │
│  │          │◄───│ Map                   │          │
│  │          │    └───────────────────────┘          │
│  │          │                                       │
│  │          │    ┌───────────────────────┐          │
│  │  Learner │◄───│ UC-02: Search &       │          │
│  │  (Actor) │    │ Retrieve Topic        │          │
│  │          │    └───────────────────────┘          │
│  │          │                                       │
│  │          │    ┌───────────────────────┐          │
│  │          │◄───│ UC-03: Take Practice  │          │
│  │          │    │ Quiz                  │          │
│  │          │    └───────────────────────┘          │
│  │          │                                       │
│  │          │    ┌───────────────────────┐          │
│  │          │◄───│ UC-04: Track Learning │          │
│  │          │    │ Progress              │          │
│  │          │    └───────────────────────┘          │
│  └──────────┘                                       │
└──────────────────────────────────────────────────────┘
```

---

## UC-01: View Syllabus Knowledge Map

| Element | Description |
|---------|-------------|
| **Use Case ID** | UC-01 |
| **Title** | View Syllabus Knowledge Map |
| **Actor** | Certified Learner |
| **Goal** | View the entire AI-901 syllabus as an interactive knowledge map |
| **Precondition** | Learner has opened the platform |
| **Postcondition** | Knowledge map is displayed; learner can see all modules and topics |

**Main Flow:**

| Step | Actor Action | System Response |
|------|-------------|-----------------|
| 1 | Learner opens the platform | |
| 2 | | System detects no certification selected; displays certification selection page |
| 3 | Learner selects "AI-901" | |
| 4 | | System loads the AI-901 syllabus structure from configuration |
| 5 | | System renders the knowledge map showing top-level modules with exam weightings |
| 6 | Learner clicks on a module to expand | |
| 7 | | System expands the module showing its sub-topics |
| 8 | Learner clicks on a sub-topic | |
| 9 | | System navigates to the topic's content view (see UC-02 for content details) |

**Alternative Flows:**

| ID | Condition | Flow |
|----|-----------|------|
| A1 | Learner has previously studied | System displays the knowledge map with progress indicators from last session (Step 4) |
| A2 | Learner selects a certification not yet available | System displays "Coming Soon" message with notification option |
| E1 | Syllabus configuration file is corrupted | System displays error message: "Unable to load syllabus. Please refresh or contact support." |

---

## UC-02: Search & Retrieve Topic Content

| Element | Description |
|---------|-------------|
| **Use Case ID** | UC-02 |
| **Title** | Search and Retrieve Topic Content |
| **Actor** | Certified Learner |
| **Goal** | Find and view content for a specific syllabus topic |
| **Precondition** | Learner is on any platform screen |
| **Postcondition** | Learner views the topic content with source citation |

**Main Flow:**

| Step | Actor Action | System Response |
|------|-------------|-----------------|
| 1 | Learner types a keyword in the search bar | |
| 2 | | System filters syllabus topics matching the keyword |
| 3 | | System displays matching topics grouped by module, within 1 second |
| 4 | Learner clicks a search result | |
| 5 | | System loads the topic's content view |
| 6 | | System displays the topic name, parent module, content body, and source citation |
| 7 | Learner reads the content | |
| 8 | Learner clicks "Mark as Reviewed" (optional) | |
| 9 | | System updates progress indicator for this topic |

**Alternative Flows:**

| ID | Condition | Flow |
|----|-----------|------|
| A1 | No matching results | System displays "No results found. Try different keywords." and suggests browsing the knowledge map |
| A2 | Learner wants a Quick Look instead of full content | System displays Quick Look popover with topic summary and "View Full Content" link |
| E1 | Network error loading topic content | System displays cached version (if available) or error message |

---

## UC-03: Take Practice Quiz

| Element | Description |
|---------|-------------|
| **Use Case ID** | UC-03 |
| **Title** | Take Practice Quiz |
| **Actor** | Certified Learner |
| **Goal** | Verify understanding of a module or topic by answering practice questions |
| **Precondition** | Learner has viewed at least one module's content |
| **Postcondition** | Learner sees quiz results with topic-level breakdown |

**Main Flow:**

| Step | Actor Action | System Response |
|------|-------------|-----------------|
| 1 | Learner navigates to a module and clicks "Practice This Module" | |
| 2 | | System generates a quiz with multiple-choice questions covering topics in that module |
| 3 | | System displays Question 1 with 4 answer options |
| 4 | Learner selects an answer and clicks "Submit" | |
| 5 | | System displays correct/incorrect indication |
| 6 | | System displays an explanation referencing the syllabus topic |
| 7 | | System advances to the next question |
| 8 | Steps 4-7 repeat until all questions are answered | |
| 9 | | System displays quiz results: overall score, score per topic, weak topics identified |
| 10 | Learner reviews results | |
| 11 | Learner clicks "Return to Module" or "Retake Quiz" | |

**Alternative Flows:**

| ID | Condition | Flow |
|----|-----------|------|
| A1 | Learner selects "Practice Weak Topics" from dashboard | System generates quiz focused only on topics where score < 70% |
| A2 | Learner exits quiz mid-way | System saves partial answers; displays "You have unanswered questions. Resume quiz?" on next visit |
| E1 | No questions available for selected topic | System displays "No practice questions available for this topic yet" |

---

## UC-04: Track Learning Progress

| Element | Description |
|---------|-------------|
| **Use Case ID** | UC-04 |
| **Title** | Track Learning Progress |
| **Actor** | Certified Learner |
| **Goal** | View overall progress across the syllabus and identify weak topics |
| **Precondition** | Learner has completed at least one study session |
| **Postcondition** | Learner understands their progress status |

**Main Flow:**

| Step | Actor Action | System Response |
|------|-------------|-----------------|
| 1 | Learner navigates to the knowledge map screen | |
| 2 | | System displays progress indicators on each module (e.g., "3/5 topics viewed") |
| 3 | | System displays overall syllabus progress (e.g., "45% complete") |
| 4 | Learner navigates to Progress Dashboard | |
| 5 | | System displays list of weak topics (topics with quiz score < 70%) |
| 6 | | System displays study streak or session history |
| 7 | Learner clicks a weak topic | |
| 8 | | System navigates to that topic's content for review |

**Alternative Flows:**

| ID | Condition | Flow |
|----|-----------|------|
| A1 | Learner has no quiz data yet | System shows "viewed" progress only; prompts learner to take a quiz |
| A2 | Learner has no weak topics | System displays "Great job! No weak topics identified." and suggests advanced practice |
| E1 | Local storage data is cleared | System treats learner as new; displays empty progress with "Welcome back or start fresh?" prompt |

---

## Use Case Summary

| ID | Name | Priority | Related FRs |
|----|------|----------|-------------|
| UC-01 | View Syllabus Knowledge Map | High | FR01-001, FR01-002, FR01-003 |
| UC-02 | Search & Retrieve Topic Content | High | FR02-001, FR02-002, FR02-003, FR02-005 |
| UC-03 | Take Practice Quiz | High | FR03-001, FR03-002, FR03-003, FR03-004 |
| UC-04 | Track Learning Progress | Medium | FR04-001, FR04-002, FR04-003 |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | Use cases assume a single actor (Learner) — authentication is not required for MVP |
| 2 | Exception flows (E1) are documented for completeness but may not be implemented in MVP |
| 3 | All use cases are testable via clickable prototype or manual testing |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | UC-02 (Search & Retrieve) should be the first use case implemented and tested — it is the core value proposition |
| 2 | Document use cases in an interview portfolio to demonstrate formal BA methodology understanding |
| 3 | Note any exception flows you chose NOT to implement and explain why (shows prioritization thinking) |
