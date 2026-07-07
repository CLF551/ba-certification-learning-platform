# Non-functional Requirements

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

---

## NFR Categories

### 1. Usability

| ID | Requirement | Priority | Rationale |
|----|-------------|----------|-----------|
| NFR01 | The knowledge map shall be fully navigable within 3 taps from any screen to any topic content. | High | Directly supports BR02 (quick retrieval); addresses the "Knowledge Gap Moment" |
| NFR02 | The search bar shall display results within 1 second of typing the third character. | High | Users in a "gap moment" are impatient — slow search = churn |
| NFR03 | The mobile version shall render all text at minimum 16px font size for readability. | Medium | Persona B studies on phone during commute |
| NFR04 | All interactive elements (buttons, links, search) shall have a minimum touch target of 44x44px on mobile. | Medium | Mobile usability standard (Apple HIG / Material Design) |

### 2. Reliability

| ID | Requirement | Priority | Rationale |
|----|-------------|----------|-----------|
| NFR05 | The system shall store all user progress data in local storage so that data persists across browser sessions. | High | Persona B studies in fragmented sessions; losing progress = churn |
| NFR06 | AI-generated content shall always display a source citation to the official Microsoft document. | High | BR06 — source traceability is a core differentiator |
| NFR07 | Practice quiz results shall be accurate to within 1% of calculated score. | Medium | Exam readiness confidence depends on reliable scoring |

### 3. Performance

| ID | Requirement | Priority | Rationale |
|----|-------------|----------|-----------|
| NFR08 | The knowledge map page shall load within 2 seconds on a standard 4G connection. | Medium | Slow loading = perceived complexity for time-poor users |
| NFR09 | AI-generated responses (if applicable) shall be displayed incrementally (streaming) rather than requiring full response load. | Low (MVP) / High (Platform) | Improves perceived speed |
| NFR10 | Topic content pages shall pre-load adjacent topics in the background for instant navigation. | Low | Enhancement for power users |

### 4. Maintainability

| ID | Requirement | Priority | Rationale |
|----|-------------|----------|-----------|
| NFR11 | The syllabus structure shall be defined in a single configuration file (e.g., JSON), not hardcoded into the UI. | High | Required for BR07 (multi-cert expansion) |
| NFR12 | Each topic's content shall be stored as an independent unit so that topics can be added, updated, or removed without affecting other topics. | Medium | AI-901 syllabus may be updated by Microsoft |
| NFR13 | The codebase shall use a consistent naming convention aligned with syllabus module IDs for traceability. | Medium | Makes future maintenance predictable |

### 5. Accessibility

| ID | Requirement | Priority | Rationale |
|----|-------------|----------|-----------|
| NFR14 | All content images and icons shall include descriptive alt text. | Low (MVP) / Medium (Platform) | Baseline accessibility practice |
| NFR15 | The system shall support keyboard navigation for all interactive features. | Low (MVP) / Medium (Platform) | WCAG 2.1 Level A compliance |

### 6. Platform Constraints

| ID | Requirement | Priority | Rationale |
|----|-------------|----------|-----------|
| NFR16 | The MVP shall be a client-side web application requiring no server-side infrastructure. | High | Project budget constraint; no backend hosting costs |
| NFR17 | The system shall work on the latest two versions of Chrome, Safari, Firefox, and Edge. | High | Covers >95% of Hong Kong users |
| NFR18 | AI features shall use free-tier API allowances where possible to minimize recurring costs. | High | Budget constraint |

---

## NFR Summary by Priority

| Priority | Count | Description |
|----------|-------|-------------|
| High | 7 | Must be in MVP |
| Medium | 7 | Should be in MVP if feasible |
| Low | 4 | Post-MVP / nice to have |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | MVP is a client-side web app; no backend, authentication, or database required |
| 2 | Browser local storage is sufficient for MVP; cloud sync is a post-MVP feature |
| 3 | Free-tier AI API allowances are sufficient for MVP user testing |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | NFR11 (syllabus as config file) is the most important NFR — without it, multi-cert expansion is impossible |
| 2 | NFR05 (local storage persistence) should be tested early — unexpected browser clearing can destroy user trust |
| 3 | Accept the accessibility (NFR14-15) limitations for MVP, but document them as known gaps |
