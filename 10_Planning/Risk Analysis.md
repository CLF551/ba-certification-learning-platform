# Risk Analysis

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Methodology

Standard BA risk assessment using Likelihood × Impact = Risk Score.

| Score | Rating | Response |
|-------|--------|----------|
| 1-3 | Low | Accept / Monitor |
| 4-6 | Medium | Mitigate |
| 7-9 | High | Mitigate / Avoid |
| 10+ | Critical | Avoid / Transfer |

---

## Risk Register

| ID | Risk Description | Category | Likelihood (1-5) | Impact (1-5) | Score | Response Strategy | Mitigation |
|----|-----------------|----------|-----------------|-------------|-------|-------------------|------------|
| R01 | Microsoft claims IP infringement for syllabus usage in the platform | Legal | 3 | 5 | **15 (Critical)** | Avoid | Use syllabus structure as reference only; do not copy verbatim content; add fair use disclaimer; cite all sources |
| R02 | Users do not see value in a syllabus-structured tool versus general AI tools | Market | 3 | 4 | **12 (High)** | Mitigate | Validate with user testing in Phase 2; focus marketing messaging on "precision" and "retrieval speed" |
| R03 | Microsoft adds AI Q&A features to Microsoft Learn, reducing market need | Competitive | 3 | 4 | **12 (High)** | Mitigate | Differentiate through multi-cert platform; focus on retrieval UX that Learn cannot match |
| R04 | AI-901 syllabus content is updated by Microsoft, requiring content maintenance | Operational | 4 | 3 | **12 (High)** | Mitigate | Design content as separate config (NFR11); update process should take < 1 hour |
| R05 | Browser local storage is cleared, user loses all progress | Technical | 3 | 3 | **9 (High)** | Mitigate | Add "Export progress" feature; warn user before clearing data; document cloud sync as future feature |
| R06 | User testing reveals Quick Look is not intuitive | UX | 4 | 2 | **8 (Medium)** | Mitigate | Add onboarding hint on first use; iterate based on feedback |
| R07 | Mobile-responsive design fails on specific devices | Technical | 3 | 2 | **6 (Medium)** | Mitigate | Test on 3+ real devices before MVP release; fix device-specific issues |
| R08 | Free-tier AI API limits reached during testing | Budget | 3 | 2 | **6 (Medium)** | Mitigate | Use content-first approach (no AI in MVP); AI features are Phase 3 |
| R09 | Hong Kong certification market is too small for sustainable use | Market | 2 | 3 | **6 (Medium)** | Accept | Portfolio project — not dependent on market size for success |
| R10 | Unable to recruit user testing participants | Operational | 2 | 2 | **4 (Low)** | Accept | Use self-testing and peer review as fallback; document as project limitation |

---

## Risk Heat Map

```
Impact
  ▲
5 │       R01
  │
4 │       R02  R03  R04
  │
3 │            R05
  │
2 │            R06  R07  R08  R09
  │
1 │                       R10
  │
  └───────────────────────────────▶ Likelihood
     1    2    3    4    5

Color Legend:
  ██ Critical (10+)  ██ High (7-9)  ██ Medium (4-6)  ██ Low (1-3)
```

---

## Top 3 Risks to Address

### Risk R01: Microsoft IP Infringement

**Why it matters:** This is the highest severity risk (15/25). If not managed, the entire project concept could be legally challenged.

**Mitigation actions:**
1. Use syllabus structure (topic names, hierarchy, weights) — these are factual and not copyrightable
2. Write original content explanations in our own words — do not copy Microsoft Learn text
3. Source titles/URLs as citations are acceptable under fair use
4. In interviews, proactively address this: "I understand IP is a concern. The platform uses the syllabus as a structural reference, and all content is originally written with source citations."

### Risk R02: Users Don't See Value

**Why it matters:** If users don't understand why this is different from ChatGPT, the product fails.

**Mitigation actions:**
1. Make the "Built on official syllabus" value proposition visible on every screen
2. Compare directly: "This is organized by exam syllabus, not by AI guess"
3. Validate with user testing before investing in full development

### Risk R03: Microsoft Learn + AI

**Why it matters:** Microsoft has the resources to add AI to Learn, potentially making our core feature redundant.

**Mitigation actions:**
1. The platform's value is not just "syllabus alignment" — it's "best retrieval UX"
2. Microsoft Learn's UX moves slowly due to enterprise constraints; we can move faster
3. Multi-cert expansion reduces dependency on Microsoft-specific content
4. In interviews: "Microsoft may add AI to Learn, but they won't optimize for every certification the way a focused platform can"

---

## Residual Risks (After Mitigation)

| ID | Residual Risk Level | Acceptable? |
|----|--------------------|-------------|
| R01 | Medium (score 6) — legal risk reduced but not eliminated | Yes, for portfolio project |
| R02 | Medium (score 6) — risk remains until user testing | Monitor during Phase 2 |
| R03 | Medium (score 6) — competitive risk persists | Accept as ongoing market dynamic |
| R04 | Low (score 3) — mitigated by architecture design | Yes |
| R05 | Low (score 3) — mitigated by export feature | Yes |
| Others | Low | Yes |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | Risk scoring is based on the project initiator's assessment, not formal quantitative analysis |
| 2 | Legal risks (R01) are assessed at the Hong Kong / common law jurisdiction level |
| 3 | Portfolio project risks are different from commercial project risks (R09 is acceptable for a portfolio) |

## Recommendations

| # | Recommendation |
|---|----------------|
| 1 | In interviews, lead with R01 (Microsoft IP) — it shows you understand the biggest business risk |
| 2 | Frame R02 and R03 together: "The two biggest risks are users not seeing value and Microsoft competing. Our strategy is multi-cert expansion and superior UX." |
| 3 | Document this risk register in your portfolio — it is one of the strongest signals of BA maturity |
