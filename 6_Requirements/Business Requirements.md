# Business Requirements

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Source Documents

- Business Problem Statement (v1.0)
- Product Vision (v1.0)
- User Personas (v1.0)
- Customer Journey Map — Sarah (v1.0)
- Competitive Analysis (v1.0)
- SWOT Analysis (v1.0)

---

## Business Requirements

| ID | Business Requirement | Source | Priority |
|----|---------------------|--------|----------|
| BR01 | The platform must allow candidates to learn certification content organized according to the official AI-901 syllabus structure. | Product Vision; Persona A, B, C | High |
| BR02 | The platform must enable candidates to retrieve any syllabus topic in the fewest possible steps when they encounter a knowledge gap. | Customer Journey Map (Stage 4 — Knowledge Gap Moment); Product Vision | High |
| BR03 | The platform must provide practice assessments that help candidates verify their understanding and identify weak topics. | Product Vision ("assessment methods aligned"); Persona B, C | High |
| BR04 | The platform must track individual learning progress across sessions and highlight areas that need attention. | Persona A (progress visibility), Persona B (session continuity), Persona C (confidence tracking) | Medium |
| BR05 | The platform must support access across devices (smartphone + laptop) to accommodate fragmented study time. | Persona B (mobile commute), Persona A (laptop primary) | Medium |
| BR06 | The platform must ensure all learning content is derived from and traceable to the official Microsoft AI-901 syllabus. | SWOT (IP risk mitigation); Competitive Analysis (source control differentiator) | High |
| BR07 | The platform must be designed with a modular architecture that can be extended to support additional certifications beyond AI-901. | Opportunity Statement (multi-cert expansion) | Low (MVP) / High (Platform) |

---

## Business Requirements Traceability

| BR ID | Maps To (Problem Statement) | Maps To (Vision) | Maps To (Persona) |
|-------|----------------------------|-------------------|-------------------|
| BR01 | Content not aligned with syllabus | Syllabus as knowledge map | Eric, Sarah, Michael |
| BR02 | Cross-validation takes too long | Fewest steps to retrieve knowledge | Sarah (Knowledge Gap Moment) |
| BR03 | No way to verify learning quality | Assessment aligned with exam | Sarah, Michael |
| BR04 | No progress organization | — | Eric, Sarah, Michael |
| BR05 | — | — | Sarah (commute), Eric (laptop) |
| BR06 | AI answers deviate from official content | Precise, reliable | All (foundational) |
| BR07 | — | Future expansion | — |

---

## Business Requirements → Design Implications

| BR ID | What This Means for Design |
|-------|---------------------------|
| BR01 | The information architecture (IA) must mirror the AI-901 syllabus structure exactly |
| BR02 | A "syllabus knowledge map" with one-tap concept access must be the primary navigation pattern |
| BR03 | Practice engine must be topic-tagged so that results can be mapped back to syllabus nodes |
| BR04 | Progress must be tracked at the concept level, not just the module level |
| BR05 | Responsive design or separate mobile experience is required |
| BR06 | AI responses must include citations to the specific official source document |
| BR07 | Certification selection must be a first-class concept in the platform architecture |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | The AI-901 official syllabus is publicly available and can be used as a structural reference |
| 2 | Candidates are willing to use a new tool if it demonstrably reduces study friction |
| 3 | Session-based progress tracking is technically feasible without user accounts (local storage) but accounts enable better personalization |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | BR07 (modular architecture) should be considered during Information Architecture design but not implemented in MVP |
| 2 | All other BRs should be addressed in MVP |
| 3 | BR02 should be the highest priority in UX design — it is the moment that determines user retention |
