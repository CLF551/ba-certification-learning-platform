# UAT Test Cases

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Scope

User Acceptance Testing (UAT) for the AI-901 Certification Learning Platform — MVP features.

Test cases are derived from User Stories and Acceptance Criteria (see 7_User Stories).

---

## Test Case Format

| Field | Description |
|-------|-------------|
| TC-ID | Unique test case identifier |
| Reference | Source User Story / AC Scenario |
| Precondition | State required before test can execute |
| Test Steps | Action sequence to execute |
| Expected Result | What should happen |
| Actual Result | Filled during testing |
| Status | ✅ Pass / ❌ Fail / ⚠️ Blocked |

---

## TC01: Certification Selection

| Field | Value |
|-------|-------|
| **TC-ID** | TC01-001 |
| **Title** | User can select AI-901 certification on first visit |
| **Reference** | US01-01 (Knowledge Map) |
| **Precondition** | First visit to platform; no previous session data |
| **Test Steps** | 1. Open platform URL<br>2. Observe the landing screen<br>3. Click "Start Learning" on AI-901 card |
| **Expected Result** | System navigates to Knowledge Map screen showing AI-901 syllabus |

### TC01-002: Coming Soon Card

| Field | Value |
|-------|-------|
| **TC-ID** | TC01-002 |
| **Title** | "Coming Soon" card displays for unlaunched certifications |
| **Reference** | W01 Wireframe |
| **Precondition** | First visit to platform |
| **Test Steps** | 1. Open platform URL<br>2. Observe the landing screen |
| **Expected Result** | A "Coming Soon" card is visible below AI-901 card |
| **Status** | — |

---

## TC02: Knowledge Map

### TC02-001: View Syllabus Modules

| Field | Value |
|-------|-------|
| **TC-ID** | TC02-001 |
| **Title** | All AI-901 modules are displayed on the knowledge map |
| **Reference** | US01-01 (AC Scenario 1) |
| **Precondition** | AI-901 certification selected |
| **Test Steps** | 1. Navigate to Knowledge Map<br>2. Observe the list of modules |
| **Expected Result** | All 5 AI-901 modules are displayed with official module names and exam weightings |

### TC02-002: Expand/Collapse Module

| Field | Value |
|-------|-------|
| **TC-ID** | TC02-002 |
| **Title** | Module expands and collapses on click |
| **Reference** | US01-01 (AC Scenario 2) |
| **Precondition** | Knowledge Map displayed |
| **Test Steps** | 1. Click on Module 1 header<br>2. Observe sub-topics appear<br>3. Click Module 1 header again<br>4. Observe sub-topics disappear |
| **Expected Result** | Sub-topics appear on first click, disappear on second click |

### TC02-003: Progress Indicators Displayed

| Field | Value |
|-------|-------|
| **TC-ID** | TC02-003 |
| **Title** | Viewed topics show ✅ indicator on the map |
| **Reference** | US01-01, US04-01 |
| **Precondition** | User has viewed at least one topic (from TC03) |
| **Test Steps** | 1. Return to Knowledge Map<br>2. Observe the module containing the viewed topic |
| **Expected Result** | The viewed topic shows ✅ indicator; the parent module shows updated progress count |

---

## TC03: Topic Content

### TC03-001: Navigate from Knowledge Map to Topic

| Field | Value |
|-------|-------|
| **TC-ID** | TC03-001 |
| **Title** | Clicking a topic on the map navigates to its content |
| **Reference** | US01-01 (AC Scenario 3) |
| **Precondition** | Knowledge Map displayed with expanded module |
| **Test Steps** | 1. Click on a sub-topic name<br>2. Observe the result |
| **Expected Result** | Topic Content view loads showing the topic name, parent module, and content body |

### TC03-002: Source Citation Displayed

| Field | Value |
|-------|-------|
| **TC-ID** | TC03-002 |
| **Title** | Topic content includes source citation |
| **Reference** | US01-02 (AC Scenario 1) |
| **Precondition** | Topic Content view is displayed |
| **Test Steps** | 1. Scroll to the bottom of the topic content<br>2. Observe the source citation |
| **Expected Result** | A source citation is visible, e.g., "[Source: Microsoft Learn — AI-901 Module 1]" |

### TC03-003: Mark as Reviewed

| Field | Value |
|-------|-------|
| **TC-ID** | TC03-003 |
| **Title** | "Mark as Reviewed" button updates progress |
| **Reference** | US04-01 |
| **Precondition** | Topic Content view is displayed; topic is not yet marked |
| **Test Steps** | 1. Click "Mark as Reviewed" button<br>2. Observe button state change<br>3. Navigate back to Knowledge Map<br>4. Observe topic indicator |
| **Expected Result** | Button shows ✅ or "Reviewed" state; Knowledge Map shows ✅ for this topic |

---

## TC04: Quick Look Popover

### TC04-001: Quick Look Appears

| Field | Value |
|-------|-------|
| **TC-ID** | TC04-001 |
| **Title** | Quick Look popover displays related topic summary |
| **Reference** | US02-02 (AC Scenario 1) |
| **Precondition** | Topic Content view is displayed with related topics |
| **Test Steps** | 1. Click "Quick Look" (👁) on a related topic link<br>2. Observe the result |
| **Expected Result** | A popover appears showing a 1-2 paragraph summary of the related topic |

### TC04-002: Close Quick Look

| Field | Value |
|-------|-------|
| **TC-ID** | TC04-002 |
| **Title** | Quick Look closes and returns to previous content |
| **Reference** | US02-02 (AC Scenario 1) |
| **Precondition** | Quick Look popover is visible |
| **Test Steps** | 1. Click the [✕] close button or tap outside the popover<br>2. Observe the result |
| **Expected Result** | Popover closes; user returns exactly to where they were on the Topic Content view |

### TC04-003: Quick Look → Full Content

| Field | Value |
|-------|-------|
| **TC-ID** | TC04-003 |
| **Title** | "View Full Content" navigates to the related topic |
| **Reference** | US02-02 (AC Scenario 1) |
| **Precondition** | Quick Look popover is visible |
| **Test Steps** | 1. Click "View Full Content" link in the popover<br>2. Observe the result |
| **Expected Result** | User navigates to the Topic Content view for the related topic |

---

## TC05: Search

### TC05-001: Search Returns Results

| Field | Value |
|-------|-------|
| **TC-ID** | TC05-001 |
| **Title** | Search returns matching syllabus topics |
| **Reference** | US02-01 (AC Scenario 1) |
| **Precondition** | User is on any platform screen |
| **Test Steps** | 1. Click the search bar<br>2. Type a keyword that exists in the syllabus (e.g., "Cognitive")<br>3. Observe search results |
| **Expected Result** | Within 1 second, search results appear showing topics matching "Cognitive", grouped by module |

### TC05-002: Navigate from Search Result

| Field | Value |
|-------|-------|
| **TC-ID** | TC05-002 |
| **Title** | Clicking a search result navigates to topic content |
| **Reference** | US02-01 (AC Scenario 2) |
| **Precondition** | Search results are displayed |
| **Test Steps** | 1. Click on a search result<br>2. Observe the result |
| **Expected Result** | User navigates directly to the Topic Content view for the selected topic |

### TC05-003: No Results

| Field | Value |
|-------|-------|
| **TC-ID** | TC05-003 |
| **Title** | "No results" message for unmatched keyword |
| **Reference** | US02-01 (AC Scenario 3) |
| **Precondition** | Search bar is active |
| **Test Steps** | 1. Type a keyword that does not exist in the syllabus (e.g., "quantum")<br>2. Observe the result |
| **Expected Result** | Message displays: "No results found. Try different keywords." |

---

## TC06: Practice Quiz

### TC06-001: Start Module Quiz

| Field | Value |
|-------|-------|
| **TC-ID** | TC06-001 |
| **Title** | User can start a quiz from a module |
| **Reference** | US03-01 (AC Scenario 1) |
| **Precondition** | Topic Content view is displayed for any topic in Module 1 |
| **Test Steps** | 1. Click "Practice This Module" button<br>2. Observe the result |
| **Expected Result** | Quiz screen loads showing Question 1 of N, with a progress bar |

### TC06-002: Answer Question and See Result

| Field | Value |
|-------|-------|
| **TC-ID** | TC06-002 |
| **Title** | User submits an answer and sees correct/incorrect feedback |
| **Reference** | US03-01 (AC Scenario 2) |
| **Precondition** | Quiz screen is displayed with a question |
| **Test Steps** | 1. Select an answer option<br>2. Click "Submit"<br>3. Observe the result |
| **Expected Result** | System displays ✅ Correct or ❌ Incorrect; shows explanation with topic reference |

### TC06-003: Complete Quiz and See Results

| Field | Value |
|-------|-------|
| **TC-ID** | TC06-003 |
| **Title** | Quiz completion shows overall score and topic breakdown |
| **Reference** | US03-01 (AC Scenario 3) |
| **Precondition** | All questions in a quiz have been answered |
| **Test Steps** | 1. Answer the last question<br>2. Observe the final screen |
| **Expected Result** | Quiz Results screen displays: overall score (e.g., "8/10 — 80%"), per-topic breakdown, weak topics identified |

---

## TC07: Progress Dashboard

### TC07-001: Progress Dashboard Displays Overall Status

| Field | Value |
|-------|-------|
| **TC-ID** | TC07-001 |
| **Title** | Progress Dashboard shows overall syllabus progress |
| **Reference** | US04-01 (AC Scenario 1) |
| **Precondition** | User has viewed some topics and completed at least one quiz |
| **Test Steps** | 1. Navigate to Progress Dashboard (from menu)<br>2. Observe the main dashboard |
| **Expected Result** | Dashboard shows: overall % complete, per-module progress bars, weak topics list |

### TC07-002: Progress Persists Across Sessions

| Field | Value |
|-------|-------|
| **TC-ID** | TC07-002 |
| **Title** | Progress persists after browser refresh |
| **Reference** | US04-01 (AC Scenario 2) |
| **Precondition** | User has viewed topics and completed a quiz |
| **Test Steps** | 1. Refresh the browser / close and reopen the platform<br>2. Observe the Knowledge Map and Progress Dashboard |
| **Expected Result** | Progress indicators match the state before the refresh |

---

## Test Summary

### Test Case Count by Feature Area

| Area | Test Cases | Priority |
|------|-----------|----------|
| Certification Selection | 2 | Medium |
| Knowledge Map | 3 | High |
| Topic Content | 3 | High |
| Quick Look | 3 | High |
| Search | 3 | High |
| Practice Quiz | 3 | High |
| Progress Dashboard | 2 | High |
| **Total** | **19** | — |

### Exit Criteria for UAT

| Criteria | Target |
|----------|--------|
| All High-priority test cases pass | 100% |
| All Medium-priority test cases pass | 100% |
| No Critical or High severity defects remain | 0 |
| User can complete the "happy path" (Map → Topic → Quiz → Results) without errors | ✅ |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | UAT is performed by the project initiator (self-testing) or 1-2 peer testers |
| 2 | Test environment is the latest version of Chrome / Edge browser |
| 3 | Mobile-specific tests should be performed on both iOS Safari and Android Chrome |

## Recommendations

| # | Recommendation |
|---|----------------|
| 1 | Run UAT in the order listed: TC01 → TC02 → ... → TC07 (flows match user journey order) |
| 2 | Document all failures with screenshot + browser version for reproducibility |
| 3 | For interview discussion: frame UAT as "I defined 19 test cases covering the 7 feature areas of the MVP, all traceable to user stories and acceptance criteria" |
