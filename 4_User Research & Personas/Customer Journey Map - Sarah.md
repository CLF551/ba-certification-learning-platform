# Customer Journey Map

## Version History

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-30 | [Project Initiator] | Initial draft |

## Persona

**Sarah Wong** — In-office IT Professional, 29, Hong Kong
Time-poor, efficiency-driven, studying for AI-901 certification.

## Scenario

Sarah decides to pursue the AI-901 certification to transition from IT support to a cloud/AI role. She has 3 hours per week for study spread across evenings and commutes. She wants to pass within 4-6 weeks.

---

## Journey Stages

| Stage                | 1. Discovery                                                                                      | 2. Sign-up & Setup                                                            | 3. Daily Learning                                                                         | 4. Knowledge Gap Moment                                                                             | 5. Practice & Assessment                                                                       | 6. Exam Readiness                                                             |
| -------------------- | ------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Goal**             | Find an efficient way to prepare for AI-901                                                       | Get started quickly with minimal setup                                        | Study in fragmented time slots                                                            | Quickly re-learn a fuzzy concept                                                                    | Verify knowledge retention                                                                     | Confirm readiness and build confidence                                        |
| **Actions**          | Searches "AI-901 study tools" on Google; finds product landing page                               | Creates account; selects AI-901 certification; sets study schedule            | Opens platform on phone during commute; reads syllabus-aligned content                    | While reading a work email about Azure, realizes she forgot a related concept; opens platform       | Takes a practice quiz on a completed module; reviews incorrect answers                         | Reviews overall progress; takes a full-length practice test; books exam       |
| **Touchpoints**      | Google Search, Product Landing Page                                                               | Sign-up Page, Certification Selection, Onboarding Wizard                      | Mobile App, Knowledge Map, Topic Pages                                                    | Mobile App, Search Bar, Concept Quick View                                                          | Quiz Engine, Answer Review, Weak Topic Dashboard                                               | Progress Dashboard, Practice Test Engine, Booking Link                        |
| **Emotions**         | 😐 Curious but skeptical — "Another learning tool?"                                               | 🙂 Hopeful — Setup was quick                                                  | 😐 Neutral to positive — Content is well-structured                                       | 😤 Frustrated — "I know I learned this, where is it?" then 🙌 Relieved when found in 2 taps         | 🙂 Satisfied — "I got 80% on this module"                                                      | 😊 Confident — Progress clearly visible; knows weak areas                     |
| **Pain Points**      | Hard to distinguish real value from marketing claims; many tools claim "AI-powered"               | Forced to set up a profile before seeing value                                | Small screen experience may be cramped; content might not be optimized for mobile reading | If search is slow or inaccurate, she will close the app and never verify (fuzzy knowledge persists) | Generic quizzes not tailored to her weak topics; no explanation for why she got it wrong       | Cannot tell if she is actually ready or just memorized the practice questions |
| **Opportunities**    | Highlight "built on official syllabus" as key differentiator; show a preview of the knowledge map | Allow anonymous browsing; offer "AI-901 only" fast track without full profile | Mobile-first content design; bookmark/resume feature for interrupted sessions             | Instant concept search across syllabus; auto-suggest related concepts; show exact syllabus location | Adaptive quizzes that weigh weak topics; answer explanations with official syllabus references | Progress % against syllabus; confidence score per topic; predict readiness    |
| **Sarah's Thoughts** | "I hope this isn't another tool that wastes my time."                                             | "OK, not bad. Let me see if the content is actually useful."                  | "This is organized like the actual syllabus... I like that."                              | "Ugh, what was that Azure Cognitive Services thing again? ... Oh wow, 2 taps and I found it."       | "Finally, a quiz that tests what I'm actually bad at."                                         | "I can see exactly what I know and what I don't. I feel ready."               |

---

## Emotional Journey Curve

```
Positive
  ^
  |                                  🙌        😊
  |                                     😊
  |  😊       😊
  |           😊
  |                        😊
  |    😐
  |                                       😐
  |        😐
  |                                        😤  (if search fails)
  |                     😤
  |  😐
Negative
  +------------------------------------------------------->
     Disc.    Sign-up   Daily     Gap      Practice   Ready
                    Learning   Moment
```

## Key Insight

**The most critical moment in Sarah's journey is the "Knowledge Gap Moment" (Stage 4).**

If the product delivers a fast, seamless experience here, Sarah becomes a loyal user. If it fails (slow search, irrelevant results), she will revert to her old workflow and may churn.

This insight will directly influence MVP feature prioritization.

---

## Assumptions

| # | Assumption |
|---|------------|
| 1 | Sarah's journey represents the most challenging use case (fragmented time, mobile usage, high forgetfulness) |
| 2 | The "Knowledge Gap Moment" is universal across all three personas |
| 3 | Candidates who feel confident during practice are more likely to book and pass the exam |

## Recommendations

| # | Recommendation |
|---|---------------|
| 1 | Design the product experience around the "Knowledge Gap Moment" — make this the hero feature |
| 2 | Optimize mobile experience for reading and searching before content creation |
| 3 | Consider an adaptive quiz engine for MVP rather than static question banks |
