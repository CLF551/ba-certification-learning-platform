# Functional Requirements

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Traceability

BR = Business Requirement (see Business Requirements.md)

This document uses the format: **FR-BRXX-YYY** (Functional Requirement for Business Requirement XX, sequential number)

---

## FR Category 1: Syllabus-based Knowledge Map (BR01, BR06)

| ID | Functional Requirement | BR Source | Priority |
|----|----------------------|-----------|----------|
| FR01-001 | The system shall display the AI-901 syllabus as an interactive knowledge map organized by the official module and topic hierarchy. | BR01 | High |
| FR01-002 | The system shall allow users to expand/collapse each module to reveal its sub-topics. | BR01 | High |
| FR01-003 | The system shall indicate the official exam weight (weighting %) for each module on the knowledge map. | BR01 | Medium |
| FR01-004 | The system shall provide content for each syllabus topic that is derived from the official AI-901 documentation. | BR06 | High |
| FR01-005 | The system shall display a source reference (official document title or URL) for each topic's content. | BR06 | High |

## FR Category 2: Quick Topic Retrieval (BR02)

| ID | Functional Requirement | BR Source | Priority |
|----|----------------------|-----------|----------|
| FR02-001 | The system shall provide a search bar accessible from any screen that searches across all syllabus topics. | BR02 | High |
| FR02-002 | The system shall return search results categorized by syllabus module, with direct links to the topic content. | BR02 | High |
| FR02-003 | The system shall provide a "Quick Look" view for any topic that displays a concise summary (1-2 paragraphs) without navigating away from the current screen. | BR02 | High |
| FR02-004 | The system shall remember the user's last-viewed topic and allow one-tap return to it. | BR02 | Medium |
| FR02-005 | From the knowledge map, the system shall allow one-tap access to any topic's full content view. | BR02 | High |

## FR Category 3: Practice Assessment (BR03)

| ID | Functional Requirement | BR Source | Priority |
|----|----------------------|-----------|----------|
| FR03-001 | The system shall provide practice quizzes composed of multiple-choice questions aligned with the AI-901 exam format. | BR03 | High |
| FR03-002 | The system shall tag each practice question to its corresponding syllabus topic. | BR03 | High |
| FR03-003 | The system shall display the user's score per topic after completing a quiz. | BR03 | Medium |
| FR03-004 | After answering a question, the system shall display an explanation referencing the relevant syllabus topic. | BR03 | High |
| FR03-005 | The system shall allow users to retake quizzes for specific topics they want to practice. | BR03 | Medium |

## FR Category 4: Progress Tracking (BR04)

| ID | Functional Requirement | BR Source | Priority |
|----|----------------------|-----------|----------|
| FR04-001 | The system shall track which syllabus topics a user has viewed. | BR04 | Medium |
| FR04-002 | The system shall track quiz performance per topic and identify topics with low scores as "weak topics." | BR04 | High |
| FR04-003 | The system shall display an overall progress indicator (e.g., "45% of syllabus covered") on the knowledge map. | BR04 | Medium |
| FR04-004 | The system shall allow users to clear or reset their progress data. | BR04 | Low |

## FR Category 5: Multi-device Access (BR05)

| ID | Functional Requirement | BR Source | Priority |
|----|----------------------|-----------|----------|
| FR05-001 | The system shall render correctly on both mobile screens (minimum 320px width) and desktop screens. | BR05 | High |
| FR05-002 | The system shall maintain reading progress and quiz data using browser local storage (MVP phase). | BR05 | Medium |
| FR05-003 | The system shall provide a mobile-optimized navigation that prioritizes quick topic retrieval. | BR05 | High |

## FR Category 6: Certification Selection (BR07 — Platform Architecture)

| ID | Functional Requirement | BR Source | Priority |
|----|----------------------|-----------|----------|
| FR06-001 | The system shall allow users to select a certification from a list of available certifications. | BR07 | Low (MVP) / High (Platform) |
| FR06-002 | The system shall load the syllabus structure corresponding to the selected certification. | BR07 | Medium (Platform) |
| FR06-003 | The system's core features (knowledge map, search, practice, progress) shall work identically across different certifications. | BR07 | Medium (Platform) |

---

## Functional Requirements Summary by Priority

| Priority | Count | Description |
|----------|-------|-------------|
| High | 12 | Must be in MVP |
| Medium | 7 | Should be in MVP if time allows |
| Low | 1 | Post-MVP (platform phase) |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | MVP will be a web-based single-page application (no native app required) |
| 2 | Browser local storage is sufficient for MVP data persistence (no backend required) |
| 3 | AI features (content generation, Q&A) can be implemented via API calls to existing LLM services |
| 4 | All FRs can be validated through a clickable prototype without production-level implementation |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | Validate FR02-001 through FR02-005 (quick retrieval) in user testing first — this is the highest-impact feature |
| 2 | FR03-005 (retake quizzes) should be prioritized if early testing shows users want repeated practice |
| 3 | FR06-001 (certification selection) should be implemented as a simple selection screen in platform phase — do not over-engineer for MVP |
