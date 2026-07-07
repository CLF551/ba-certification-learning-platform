# User Stories & Acceptance Criteria

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Epic Structure

| Epic ID | Epic Name | Related BRs | Priority |
|---------|-----------|-------------|----------|
| E01 | Syllabus-based Learning | BR01, BR06 | High |
| E02 | Quick Knowledge Retrieval | BR02 | High |
| E03 | Practice & Assessment | BR03 | High |
| E04 | Progress Tracking | BR04 | Medium |
| E05 | Multi-device Experience | BR05 | Medium |

---

## E01: Syllabus-based Learning

### US01-01: View Syllabus Knowledge Map

**As a** certification candidate,
**I want to** see the entire AI-901 syllabus as a visual knowledge map organized by module,
**so that** I understand what I need to learn and how topics are structured.

**Acceptance Criteria:**

```
Scenario 1: View syllabus map on desktop
  Given I am a new user on the platform
  When I land on the home page
  Then I should see the AI-901 syllabus displayed as an expandable knowledge map
  And each module should be shown with its official module name
  And I should see the exam weighting (%) next to each module

Scenario 2: Expand and collapse modules
  Given I am viewing the knowledge map
  When I click on a module name
  Then the module should expand to show its sub-topics
  And when I click again, the module should collapse

Scenario 3: Navigate to topic content
  Given I am viewing the expanded knowledge map
  When I click on a sub-topic
  Then I should be taken to the full content view for that topic
```

### US01-02: View Topic Content with Source Reference

**As a** certification candidate,
**I want to** see detailed content for each syllabus topic with a reference to the official Microsoft source,
**so that** I can trust the content is accurate and know where to verify it.

**Acceptance Criteria:**

```
Scenario 1: View topic content
  Given I have navigated to a specific syllabus topic
  Then I should see the topic's content displayed in a readable format
  And I should see a source citation indicating which official document the content is derived from
  And the source citation should include the document title or URL

Scenario 2: Content is syllabus-aligned
  Given I am viewing any topic's content
  Then the content should cover only concepts within that topic's scope as defined by the official syllabus
  And should not include concepts from other modules or out-of-scope topics
```

---

## E02: Quick Knowledge Retrieval

### US02-01: Search Syllabus Topics

**As a** learner who has a fuzzy concept in mind,
**I want to** type a keyword and instantly see matching topics from the syllabus,
**so that** I can quickly find and review the exact topic I need without browsing through modules.

**Acceptance Criteria:**

```
Scenario 1: Search returns syllabus topics
  Given I am on any page of the platform
  When I type a keyword in the search bar
  Then I should see a list of syllabus topics matching my keyword within 1 second
  And each result should display the topic name and its parent module
  And results should be ordered by relevance

Scenario 2: Navigate from search result
  Given I see search results for my keyword
  When I click on a search result
  Then I should be taken directly to the full content view of that topic

Scenario 3: Search with no results
  Given I type a keyword that does not match any syllabus topic
  When I submit the search
  Then I should see a "No results found" message
  And a suggestion to try different keywords
```

### US02-02: Quick Look at Topic from Any Screen

**As a** learner in the middle of studying a topic,
**I want to** quickly preview a related topic without leaving my current page,
**so that** I can resolve a knowledge gap without disrupting my flow.

**Acceptance Criteria:**

```
Scenario 1: Quick Look from topic content
  Given I am viewing a topic's content that contains a reference to another topic
  When I click on a linked topic or search result preview
  Then I should see a "Quick Look" popover with a 1-2 paragraph summary
  And the popover should have a "View Full Content" button for detailed study
  And when I close the popover, I should return exactly to where I was

Scenario 2: Quick Look from knowledge map
  Given I am viewing the knowledge map
  When I hover over or tap a sub-topic
  Then I should see a Quick Look preview of that topic
  Without navigating away from the knowledge map
```

---

## E03: Practice & Assessment

### US03-01: Take Topic-specific Quiz

**As a** learner who has completed a syllabus module,
**I want to** take a practice quiz on that specific module,
**so that** I can verify whether I understood the content before moving to the next module.

**Acceptance Criteria:**

```
Scenario 1: Start a quiz from a module
  Given I have viewed at least one syllabus module
  When I click "Practice This Module" on a module
  Then I should see a quiz with multiple-choice questions covering topics in that module
  And the number of questions should be appropriate for the module size (minimum 3 questions)

Scenario 2: Answer questions and get results
  Given I am taking a quiz
  When I select an answer and submit
  Then I should see whether my answer was correct or incorrect
  And I should see an explanation referencing the relevant syllabus topic
  And my score for that module should be updated

Scenario 3: View topic-level results
  Given I have completed a quiz
  When I view my quiz results
  Then I should see my score broken down by topic within the module
  And topics where I scored below 70% should be marked as "weak topics"
```

### US03-02: Retake Practice on Weak Topics

**As a** learner who identified my weak areas,
**I want to** retake practice questions specifically on my weak topics,
**so that** I can focus my revision time where it matters most.

**Acceptance Criteria:**

```
Scenario 1: Practice weak topics
  Given I have completed at least one quiz and have identified weak topics
  When I navigate to my weak topics list
  Then I should see a "Practice Weak Topics" option
  And clicking it should generate a quiz focused on topics where I scored below 70%

Scenario 2: Weak topics update after retake
  Given I retake a quiz on previously weak topics
  When I complete the quiz and score above 70%
  Then the system should update that topic's status and remove it from the weak topics list
```

---

## E04: Progress Tracking

### US04-01: View Learning Progress

**As a** learner studying over multiple sessions,
**I want to** see my overall progress across the syllabus,
**so that** I know how much I have covered and what remains.

**Acceptance Criteria:**

```
Scenario 1: View progress on knowledge map
  Given I have viewed some syllabus topics
  When I look at the knowledge map
  Then each module should show a progress indicator (e.g., "3/5 topics viewed")
  And the overall syllabus should show a percentage complete

Scenario 2: Progress persists across sessions
  Given I studied some topics yesterday and closed the browser
  When I return to the platform today
  Then my progress indicators should still show yesterday's completed topics
  And I should see my last-viewed topic highlighted
```

---

## E05: Multi-device Experience

### US05-01: Study on Mobile

**As a** learner who studies during commute,
**I want to** access all platform features on my phone,
**so that** I can use my travel time effectively.

**Acceptance Criteria:**

```
Scenario 1: Knowledge map on mobile
  Given I am accessing the platform on a smartphone (320px - 768px width)
  When I view the knowledge map
  Then the modules should be displayed in a vertically scrollable list
  And each module should be tappable to expand/collapse
  And sub-topics should be large enough to tap (minimum 44x44px)

Scenario 2: Topic content readable on mobile
  Given I am reading topic content on a smartphone
  Then the text should render at minimum 16px font size
  And the content should fit within the screen width without horizontal scrolling

Scenario 3: Search on mobile
  Given I am on a smartphone and tap the search icon
  Then the search bar should expand and the keyboard should appear
  And results should be displayed in a scrollable list
```

---

## User Story Mapping (MVP Scope)

```
          ┌─────────────────────────────────────────────────────┐
          │                    MVP RELEASE                      │
          ├─────────────────────────────────────────────────────┤
Layer 1   │  US01-01: View Syllabus Map                         │
Backbone  │  US01-02: View Topic Content with Source            │
          │  US02-01: Search Topics                              │
          │  US02-02: Quick Look Preview                        │
          ├─────────────────────────────────────────────────────┤
Layer 2   │  US03-01: Take Topic-specific Quiz                  │
Needed    │  US04-01: View Learning Progress                    │
          │  US05-01: Study on Mobile                           │
          ├─────────────────────────────────────────────────────┤
Layer 3   │  US03-02: Retake Practice on Weak Topics            │
Nice      │                                                      │
          └─────────────────────────────────────────────────────┘
```

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | User stories assume the platform is a client-side web app with no authentication requirement for MVP |
| 2 | "Progress" is tracked via browser local storage — cloud sync is post-MVP |
| 3 | All AC scenarios are testable via a clickable prototype or manual testing |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | Start development with Layer 1 stories — they define the core value proposition |
| 2 | US02-02 (Quick Look) should be validated with users as early as possible — it is the highest-risk assumption |
| 3 | Acceptance Criteria should be reviewed by a QA resource (if available) or self-tested systematically |
