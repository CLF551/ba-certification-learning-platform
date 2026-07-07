# Future Enhancements

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Purpose

This document captures features and capabilities identified during the BA process that are explicitly **out of scope for MVP**, but are logical extensions of the platform. Including this in the portfolio demonstrates **strategic thinking** — you didn't just stop at MVP, you thought about where the product goes next.

---

## Enhancement Register

| ID | Enhancement | Rationale | Dependencies | Estimated Complexity | Priority (Post-MVP) |
|----|------------|-----------|-------------|---------------------|-------------------|
| FE01 | **Multi-certification support** | Core platform expansion; reduces dependency on Microsoft alone | Modular architecture (NFR11); certification selection UI | High | P0 (Highest) |
| FE02 | **Cloud sync & user accounts** | Enables progress persistence across devices and sessions | Backend infrastructure; authentication system | High | P0 |
| FE03 | **AI-powered Q&A assistant** | Natural language Q&A within syllabus scope | LLM API integration; syllabus-scoping mechanism | Medium | P1 |
| FE04 | **Adaptive quiz engine** | Dynamic question selection based on weak topic weighting | Quiz data collection; weighting algorithm | Medium | P1 |
| FE05 | **Study streak & gamification** | Engagement features: daily streak, achievement badges, study goals | Progress tracking data; notification system | Low | P2 |
| FE06 | **Exam simulation mode** | Full-length timed exam that mirrors actual AI-901 format | Question bank expansion; timer UI; scoring logic | Medium | P1 |
| FE07 | **Content version tracking** | Track when Microsoft updates the syllabus and highlight changed topics | Version comparison logic; notification system | Medium | P2 |
| FE08 | **Downloadable study notes (PDF)** | Export topic summaries as PDF for offline study | PDF generation library; template design | Low | P2 |
| FE09 | **Community features** | Discussion forums, study groups, shared notes | User accounts; moderation system | High | P3 |
| FE10 | **Admin content dashboard** | Allow non-technical content updates without code changes | Backend CMS; role-based access | High | P2 |
| FE11 | **Dark mode** | User preference for low-light study sessions | CSS theme variables | Low | P3 |
| FE12 | **AI-generated mnemonic devices** | Help users remember key concepts through memory aids | LLM integration | Low | P3 |
| FE13 | **LinkedIn certification sharing** | Allow users to share their study progress or completion on LinkedIn | Social API integration | Low | P3 |
| FE14 | **Multi-language support** | Content in Cantonese / Mandarin for Hong Kong market | i18n framework; translation effort | Medium | P2 |
| FE15 | **Institutional version for schools** | Let teachers create custom syllabi and control AI response scope for classroom use; includes teacher dashboard and student progress monitoring | Multi-cert architecture (FE01); user accounts (FE02); admin dashboard (FE10) | High | P3 |

---

## Priority Matrix (Post-MVP)

```
                    HIGH Value
                        │
                        │
              FE01 ⭐   │  FE02 ⭐
              FE03      │  FE04
              FE06      │
                        │
    LOW Effort ─────────┼───────────────── HIGH Effort
                        │
              FE05      │  FE09
              FE08      │  FE10
              FE11      │  FE07
              FE12      │  FE14
              FE13      │
                        │
                    LOW Value
```

⭐ = Recommended for next phase

---

## Top 3 Recommended After MVP

### 1. Multi-certification Support (FE01)

**Why next:** This is the platform's long-term moat. Once you support AZ-900, DP-900, and other entry-level Microsoft certs, the platform becomes a destination rather than a one-off tool.

**Approach:** The architecture is already designed for this (NFR11 — syllabus as config file). Adding a new certification requires:
1. A new syllabus JSON configuration
2. Content written for each topic
3. Practice questions tagged to topics

### 2. Cloud Sync & User Accounts (FE02)

**Why next:** Local storage is a known weakness (R05 in Risk Analysis). Users who accidentally clear their browser data lose everything. Cloud sync also enables the business model (subscription-based access).

**Approach:** Start with simple email-based accounts; sync progress via a lightweight backend (e.g., Firebase).

### 3. AI-powered Q&A Assistant (FE03)

**Why next:** The original problem discovery identified AI answer deviation as a core pain point. Once the platform has syllabus-scoped content, an AI assistant that answers questions strictly within syllabus boundaries completes the value proposition.

**Approach:**
- User types a question → AI generates answer
- Answer must include source citation (Module X, Topic Y)
- AI is prompted with the syllabus structure and scope boundaries
- If question is out of scope, AI responds: "This topic is outside the AI-901 syllabus"

---

## Enhancements Rejected (Not Planned)

| Enhancement | Reason for Rejection |
|-------------|---------------------|
| Native mobile app (iOS/Android) | Web app with responsive design covers MVP needs; native app adds significant cost without proportional value |
| Video lessons / multimedia content | Content production cost is high; text-based + quiz approach is validated for exam prep |
| Instructor-led live classes | Changes the product category from "self-paced tool" to "training platform"; out of scope |
| Marketplace for tutors | Different business model; platform would need trust & safety infrastructure |

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | All enhancements are conceptual and have not been validated with users |
| 2 | Complexity estimates are relative (Low/Medium/High) within a web-app context |
| 3 | Business model considerations (pricing, subscription) are intentionally deferred — this is a BA portfolio project, not a funded startup |

## Recommendations

| # | Recommendation |
|---|----------------|
| 1 | In interviews, mention 2-3 future enhancements to show you've thought beyond MVP |
| 2 | Lead with Multi-cert (FE01) — it demonstrates platform thinking, not single-product thinking |
| 3 | Be honest that these are "identified but not validated" — shows BA rigor |
