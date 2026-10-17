# Bedside: The Evidence

---

## 1. The Problem

Every year 35,000 new medical students enter US programs and must learn to deliver devastating news:
cancer diagnoses, stillbirths, end-of-life conversations. The training method is standardized patients (SPs),
hired actors who roleplay being sick. A single 15-minute SP encounter costs $120-200 all-in. Students get
1-3 reps in four years. Then they do it for real, on a real family, with no one watching. 40% of malpractice
claims trace to communication failures, not clinical errors.

---

## 2. Key Numbers

### Market size

| Metric | Number | Source |
|---|---|---|
| MD students enrolled (2025-26) | 100,723 | AAMC FACTS |
| DO students enrolled (2025-26) | 40,806 | AACOM |
| Total MD+DO enrolled | ~141,500 | AAMC + AACOM |
| New MD+DO students/year | ~35,000 | AAMC (23,440 MD) + AACOM (11,538 DO) |
| MD+DO graduates/year | ~31,000 | AAMC (22,189) + AACOM (9,019) |
| US MD-granting programs | 159 | AAMC |
| US DO-granting programs | 38 | AACOM |
| US nursing programs | ~1,900 | AACN |
| US PA programs | ~300 | ARC-PA |
| US residency programs | ~12,000 | ACGME |
| Nursing/PA/residency students/year | ~400,000 | aggregate |

### Cost of current training

| Metric | Number | Source |
|---|---|---|
| SP encounter duration | 15-20 minutes | Texas Tech OSCE Manual |
| All-in cost per student per encounter | $120-200 | em-consulte (surgical OSCE study) |
| Cost per minute (implied) | ~$8/min | derived |
| First OSCE session (10 residents) | $6,649 total ($664/resident) | em-consulte |
| Each additional session (SP time only) | $1,540 | em-consulte |
| SP actor hourly rate | $15-50/hr | Mercer University, vendor estimates |
| SP training time per actor | 15-20 hours | Mercer University |
| Annual SP budget per med school | $200K-500K | SSH estimates |
| Global clinical simulation market | ~$2.5B | market reports |

### Impact numbers

| Metric | Number | Source |
|---|---|---|
| Malpractice claims from communication | 30-40% | CRICO/Harvard |
| Patient recall after oncology consult | ~40-50% of information | oncology communication literature |
| Practice reps per student (SIC) | 1-3 in 4 years | medical education literature |
| Step 2 CS (national comm skills exam) | cancelled January 2021 | USMLE |

### Bedside economics

| Metric | Number |
|---|---|
| Cost per Bedside session (API) | ~$0.04-0.08 |
| Cost reduction vs SP | 99.95% |
| Infrastructure required | one HTML file, any browser |
| Backend required | none |
| Build step required | none |

---

## 3. SOPHIE Paper

**Paper:** "AI Standardized Patient Improves Human Conversations in Advanced Cancer Care"
**Authors:** Haut, Hasan, Carroll, Epstein, Sen, Hoque (University of Rochester)
**Published:** May 2025, arXiv:2505.02694
**Study design:** Randomized controlled trial, 51 participants (26 SOPHIE, 25 control)

### What SOPHIE proved

- AI patient training **works**. SOPHIE users improved significantly across all communication skills.
- Effect sizes were **large** (Cohen's d = 0.85 to 1.61) vs medium in control (0.45 to 0.48).
- All p-values < 0.004 for the SOPHIE arm.
- Feedback quality rated **4.7/5** (highest rated feature).
- Usability rated **4.2/5**.
- Confidence gains were **13% higher** in SOPHIE group.
- Results emerged from sessions **under 30 minutes**.

### What SOPHIE got wrong (our opportunity)

- Avatar realism rated **3.4/5** (lowest rated feature). Users called it "creepy" and "uncanny."
- Long-term skill retention **unmeasured** (they flag this explicitly).
- Measures only **what the doctor said**, not what the patient understood.
- **One scenario only** (advanced lung cancer).
- Requires **Unreal Engine 5.1, Metahuman, motion capture, dedicated server**.
- Used **GPT-3.5-turbo** (outdated).

### Key quote from the paper

> "Participants prioritized SOPHIE's actionable feedback (rated 4.7/5) over the avatar's
> visual realism (3.4/5), suggesting that the training's value depends more on the quality
> of guidance than on photorealistic visuals."

This validates our design choice: cartoon face, great feedback > photorealistic avatar, same feedback.

---

## 4. Competitive Landscape

| Player | What | Strength | Weakness |
|---|---|---|---|
| **Human SPs** | Actors roleplay patients | Gold standard, real human | $120+/session, 1-3 reps/4 years, scheduling, fatigue |
| **SOPHIE** (Rochester) | AI patient, 3D avatar, RCT-validated | Proven in peer-reviewed trial | Research project not product. Unreal Engine. One scenario. |
| **Kognito** | Commercial AI patient sims | Established, enterprise sales | Broad (not SIC-focused), no hidden emotional state, no intent-vs-impact |
| **Bedside** | AI patient, hidden emotional state, SPIKES scorecard | One HTML file, $0.04/session, multiple scenarios | New, unproven at scale, needs pilot data |

---

## 5. Positioning

### Validated by research, built for real-world access

SOPHIE proved that AI patient training produces statistically significant learning gains (p < 0.004).
Their own participants rated feedback quality (4.7/5) 38% higher than avatar realism (3.4/5).
Bedside is designed around that finding.

| Dimension | Prior art | Bedside |
|---|---|---|
| Infrastructure | Unreal Engine 5.1, Metahuman, dedicated server | One HTML file, any browser |
| Cost per session | $120-200 (human SP) | $0.04-0.08 |
| Scenario coverage | Single scenario (lung cancer) | Multiple scenarios, extensible |
| Deployment | IT involvement, scheduling, facility | Student opens a link tonight |
| Feedback model | SPIKES-based (same) | SPIKES-based + hidden emotional state + intent-vs-impact analysis |

### Core thesis

The scientific question, "Does AI patient training work?", is answered. The remaining question is access and cost. Bedside answers both.

---

## 6. FAQ

**"Isn't this just ChatGPT with a prompt?"**
The patient maintains a hidden trust and emotion state that moves based on specific communication
behaviors. The grader uses SPIKES, the protocol schools already assess against. The value is
scenario design and feedback design, not the model.

**"Who pays?"**
Med schools, out of existing simulation budgets. Students use it free (that's distribution).
Schools pay for cohort analytics and faculty dashboards. $15K-30K/year institutional license
vs $100K+ current SP spend.

**"Why won't schools just build this?"**
Sim centers are staffed by educators, not engineers. They're already stretched. They buy tools.

**"Why now?"**
Three things converged: Step 2 CS cancelled in 2021 (no national comm skills exam anymore),
LLMs crossed the realism threshold in 2024-2026, and SOPHIE proved the concept in a
peer-reviewed RCT in 2025.

**"What's the moat?"**
Scenario library, scoring calibrated against real faculty ratings, and institutional data.
Every session makes the grader better. Plus the buyer pool is 197 programs. You can reach
every single one through 2-3 conferences. This is a vertical SaaS play, not a consumer product.

**"What about safety?"**
Bedside doesn't give medical advice. The patient only knows what the student tells them.
The grader evaluates communication, not clinical decisions. No patient data involved.

**"How big is this?"**
Beachhead: 197 MD+DO programs. Expansion: 1,900 nursing + 300 PA + 12,000 residency programs.
That's 400,000+ additional students/year. Adjacent: vet schools, social work, chaplaincy, law.

**"Do you have evidence it works?"**
SOPHIE's RCT (same concept, heavier infrastructure) showed large effect sizes across all
communication skills (p < 0.004). We plan pilot studies in Year 1. The scientific question
"does AI patient training work?" is answered. The product question is accessibility and cost.

---

## 7. Sources

### Research papers
- Haut et al. (2025). "AI Standardized Patient Improves Human Conversations in Advanced Cancer Care." arXiv:2505.02694. https://arxiv.org/abs/2505.02694

### SP cost data
- em-consulte: Cost and logistics for implementing the American College of Surgeons/Association of Program Directors in Surgery simulation-based surgical skills curriculum. https://www.em-consulte.com/article/944024
- BMC Research Notes: SP training cost breakdown. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4059457/
- Temple University: SP cost comparison study. https://sites.temple.edu/catafc24/files/2024/01/CAT-Annual-Meeting-Simulation-Poster-1.pdf
- Mercer University: SP program costs. https://den.mercer.edu/070313med

### Encounter duration
- Texas Tech OSCE Manual (15-min encounters). https://www.ttuhsc.edu/medicine/academic-affairs/documents/step/Third_Year_OSCE_Manual_2022-2023.pdf

### Market data
- AAMC FACTS (MD enrollment, graduates, program count). https://www.aamc.org/data-reports/students-residents/data/facts-enrollment-graduates-and-md-phd-data
- AACOM (DO enrollment, graduates). https://www.aacom.org/reports-programs-initiatives/aacom-reports
- CRICO/Harvard (malpractice and communication). https://www.rmf.harvard.edu/

### Competitors
- Kognito (commercial AI patient simulations). https://kognito.com
- SOPHIE system (University of Rochester). Referenced in arXiv paper above.

### Regulatory
- USMLE Step 2 CS discontinuation (2021). https://www.usmle.org/frequently-asked-questions

---

*Last updated: 2026-10-18. DiversaTech hackathon at UC Berkeley.*
