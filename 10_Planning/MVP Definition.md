# MVP Definition

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## What is MVP for This Project?

Since this is a BA portfolio project, the MVP represents:

> **The smallest set of features that can demonstrate the core value proposition — syllabus-aligned learning — to a user.**

The MVP is a **clickable prototype or functional web app** that validates the central hypothesis:

> "A syllabus-structured knowledge map with one-tap retrieval provides a better certification learning experience than general-purpose AI tools or browsing official docs alone."

---

## MVP Scope

### In Scope (MVP Must Have)

| Feature | Wireframe | User Story | Priority Rationale |
|---------|-----------|------------|-------------------|
| Certification Selection page | W01 | — | Entry point; 1 screen |
| Knowledge Map with expand/collapse | W02 | US01-01 | Core navigation; demonstrates syllabus alignment immediately |
| Topic Content view with source citation | W03 | US01-02 | Core value delivery; proves "syllabus-aligned content" |
| Global Search across topics | W02 (search) | US02-01 | Addresses the Knowledge Gap Moment |
| Quick Look popover | W04 | US02-02 | Minimizes friction for gap resolution |
| Practice Quiz (module-level) | W05, W06 | US03-01 | Verifies learning; demonstrates assessment alignment |
| Basic Progress Tracking (viewed topics) | W02 (indicators) | US04-01 | Shows value of tracking across sessions |
| Mobile-responsive layout | All | US05-01 | Covers Persona B's use case |

### Out of Scope (MVP)

| Feature | Reason | Planned For |
|---------|--------|-------------|
| User authentication / accounts | Local storage sufficient for MVP; authentication adds complexity | Post-MVP |
| Cloud sync across devices | Requires backend infrastructure | Post-MVP |
| Adaptive quiz engine (weak-topic weighting) | Manual quiz selection sufficient for validation | Post-MVP (Phase 2) |
| Multi-certification support | MVP validates with one certification only | Post-MVP (Phase 2) |
| AI chat / Q&A feature | Content-first approach; AI chat adds complexity and cost | Post-MVP (Phase 2) |
| Study streak / gamification | Nice-to-have; not core to value proposition | Post-MVP (Phase 3) |
| Admin dashboard / content management | No admin users in MVP | Post-MVP (Phase 3) |

---

## MVP Success Criteria

| Criteria | Target | How to Measure |
|----------|--------|----------------|
| Knowledge Gap resolution time | < 30 seconds (from opening app to viewing answer) | Timed user test (prototype) |
| User can find any topic within 3 taps | 100% of test topics | Manual test with 5 sample topics |
| User understands the syllabus structure after first visit | Self-reported 4/5 | Post-test survey |
| User completes a practice quiz | 100% completion rate | Prototype analytics |

---

## MVP Assumptions (Highest Risk)

| Risk Level | Assumption | Mitigation if Wrong |
|------------|-----------|-------------------|
| 🔴 High | Users understand and value the "syllabus-as-knowledge-map" concept | Add onboarding tooltip explaining the map |
| 🔴 High | Quick Look popover is intuitive (users will use it without instruction) | Add a subtle "tap for preview" hint on first use |
| 🟡 Medium | Users will take practice quizzes voluntarily (no external motivation) | Lower quiz friction; make it a prominent CTA from topic view |
| 🟡 Medium | Browser local storage is sufficient for a meaningful "progress" experience | Document that cloud sync is a natural extension |
| 🟢 Low | Mobile-responsive layout is enough (no native app needed for MVP) | Test on actual mobile browser, not just resize |

---

## MVP Delivery

| Deliverable | Description |
|-------------|-------------|
| **Clickable Prototype** (Primary) | Interactive wireframe in Figma/Draw.io that simulates navigation flows (W01 → W02 → W03 → W05 → W06) |
| **Functional Web App** (Optional) | A simple HTML/CSS/JS single-page app with real content for 1-2 modules to demonstrate functionality |

For a BA portfolio, the **clickable prototype** is sufficient and appropriate. The functional web app would be a bonus.

---

## Recommendations

| # | Recommendation |
|---|----------------|
| 1 | Build the prototype navigation flow in this order: W01 → W02 → W03 → W04 → W02 → W05 → W06 (this covers the full "happy path") |
| 2 | Populate W03 (Topic Content) with real AI-901 content for at least 2 modules to make the prototype feel authentic |
| 3 | In interviews, explain MVP scope decisions using the "Value vs Effort" framework — show you know what to cut |
