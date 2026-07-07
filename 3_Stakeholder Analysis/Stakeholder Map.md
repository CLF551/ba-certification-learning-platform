# Stakeholder Map

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Visual Stakeholder Map

```
                         ┌─────────────────┐
                         │  Microsoft (S03) │
                         │  IP Owner /      │
                         │  Cert Authority  │
                         └────────┬────────┘
                                  │ IP & Quality
                                  │ Concerns
                                  ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Development   │    │   Product Team   │    │  Legal Counsel  │
│   Team (S06)    │◄──►│  BA/PM (S01,S05) │◄──►│     (S08)      │
│  (Hypothetical) │    │                  │    │  (Hypothetical) │
└────────┬────────┘    └────────┬────────┘    └────────┬────────┘
         │                      │                      │
         │                      ▼                      │
         │              ┌─────────────────┐            │
         │              │  Certification  │            │
         ├─────────────►│   Candidates    │◄───────────┘
         │              │  (S02 - Users)  │            │
         │              └────────┬────────┘            │
         │                      │                      │
         ▼                      ▼                      ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│  UX Designer    │    │   Customer      │    │    Training     │
│     (S07)       │    │   Support (S09) │    │   Partners      │
│  (Hypothetical) │    │  (Hypothetical) │    │    (S10)        │
└─────────────────┘    └─────────────────┘    └─────────────────┘


                        ┌─────────────────┐
                        │   Portfolio     │
                        │   Reviewer /    │
                        │ Hiring Manager  │
                        │     (S04)       │
                        └─────────────────┘
```

## Relationships & Dependencies

| From | To | Relationship Type | Description |
|------|----|-------------------|-------------|
| Product Team | Candidates | Value Delivery | Product team designs platform to serve candidates' learning needs |
| Product Team | Microsoft | Risk/Compliance | Must address IP and quality concerns before launch |
| Product Team | Dev Team (hypo) | Dependency | Requirements must be clear and feasible for development |
| Product Team | Legal (hypo) | Advisory | Legal counsel advises on syllabus usage terms |
| Product Team | Reviewer | Evaluation | Portfolio quality influences hiring decision |
| Candidates | Product Team | Feedback | User feedback drives product iteration |
| Dev Team | UX Designer (hypo) | Collaboration | UI implementation depends on design specifications |

## Notes

- Solid lines = Actual relationships in the portfolio project context
- Dotted annotations = Relationships that would exist in a real company implementation
- The Portfolio Reviewer is a unique stakeholder — they do not influence the product itself, but influence whether the project achieves its goal (demonstrating BA competency)
