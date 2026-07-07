# Stakeholder Register

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Classification

This project is a **Business Analysis portfolio project** (not a live commercial product). Stakeholders are classified into two categories:

| Category | Definition |
|----------|------------|
| **Actual** | Entities that genuinely interact with or influence this project in its current form |
| **Hypothetical** | Entities that would exist in a real company setting; included to demonstrate BA methodology |

---

## Stakeholder Register

| ID | Stakeholder | Category | Role/Interest | Key Concerns | Power | Interest |
|----|-------------|----------|---------------|--------------|-------|----------|
| S01 | Project Initiator (Me) | Actual | Defines vision, owns deliverables | Build a convincing portfolio; demonstrate BA competency; finish the project | High | High |
| S02 | Certification Candidates (Users & Payers) | Actual | Primary users; pay for the product | Learning content aligned with syllabus; convenient knowledge retrieval; affordable pricing | Low | High |
| S03 | Microsoft | Actual | IP owner of AI-901 syllabus; certifying authority | Unauthorized use of syllabus; inaccurate content damaging certification brand | High | Medium |
| S04 | Portfolio Reviewer / Hiring Manager | Actual | Reads/discusses this portfolio in interviews | Quality of BA thinking; completeness of methodology; realism of project | High | Medium |
| S05 | Product Manager / BA (Me in real company) | Hypothetical | Owns product strategy and requirements | Prioritization trade-offs; stakeholder alignment; go-to-market | High | High |
| S06 | Development Team | Hypothetical | Builds the product | Clear requirements; realistic scope; technical feasibility | Medium | Medium |
| S07 | UX/UI Designer | Hypothetical | Designs user experience and interface | User research; interaction design; accessibility | Low | High |
| S08 | Legal Counsel | Hypothetical | IP and compliance review | Syllabus licensing; terms of service; data privacy | High | Low |
| S09 | Customer Support | Hypothetical | Handles user inquiries | Known error messages; FAQ documentation; escalation path | Low | Medium |
| S10 | Certification Training Partners | Hypothetical | Resell or recommend the platform | Revenue share; brand trust; student outcomes | Low | Medium |
| S11 | Schools / Teachers | Hypothetical (Future) | Potential B2B customer; use platform for curriculum-scoped AI learning | Classroom management; teacher control over AI scope; student progress monitoring | Low | Low |

---

## Power/Interest Grid

```
                    INTEREST
                  Low        High
          +----------------------+
   High   |  S08 (Legal)    |  S01 (Initiator)      |
          |  S04 (Reviewer) |  S05 (PM/BA - hypo)   |
  POWER    |                  |                        |
          |  S03 (Microsoft) |  S02 (Candidates)      |
   Low    |  S09 (Support)  |  S07 (UX Designer -    |
          |  S10 (Partners) |      hypo)             |
          |                  |  S06 (Dev Team - hypo) |
          +----------------------+
```

### Engagement Strategy by Quadrant

| Quadrant | Stakeholders | Strategy |
|----------|-------------|----------|
| **High Power, High Interest** | S01, S05 | Manage Closely — actively involved in all decisions |
| **High Power, Low Interest** | S03, S04, S08 | Keep Satisfied — engage periodically; address concerns proactively |
| **Low Power, High Interest** | S02, S06, S07 | Keep Informed — regular updates; seek input |
| **Low Power, Low Interest** | S09, S10 | Monitor — minimal effort, but check for changes |

---

## Key Insight for Microsoft

Microsoft plays a dual role:
- **As IP owner**: Concern about unauthorized syllabus use → requires licensing or fair use strategy
- **As certification authority**: Concern about content accuracy → requires quality assurance mechanism

This dual role makes Microsoft the **highest-risk stakeholder** to ignore.

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | The project will use Microsoft's publicly available AI-901 syllabus document as reference — this may require review of Microsoft's terms of use |
| 2 | In a real company, legal counsel would be engaged to assess IP risk before development |
| 3 | Portfolio reviewers value methodology demonstration over feature depth |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | Document Microsoft's IP concerns in the Risk Analysis section |
| 2 | In interviews, mention that a real implementation would require Microsoft partnership or syllabus licensing |
| 3 | Use the Hypothetical stakeholder categories proactively in interviews to show awareness of real-world project dynamics |
