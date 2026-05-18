# ux-audit-skill

**A structured UX audit skill for Claude Code, Cursor, and any Claude-powered workflow.**

Built by [Alif Noushad](https://alifnoushad.com) — Senior Experience Designer at IBM iX, with 6+ years of enterprise UX delivery across automotive, retail, and financial services.

---

## What It Does

Runs any digital interface through a 28-rule audit framework covering:

- **Visual and structural quality** — consistency, component discipline, layout completeness
- **UX heuristics** — Nielsen's 10 + Laws of UX (Fitts, Hick, Miller, Jakob, Postel, and more)
- **WCAG 2.1 / 2.2 accessibility** — all four POUR principles, including the new target size criterion from WCAG 2.2
- **Behavioural psychology** — Peak-End Rule, Goal-Gradient Effect, Von Restorff, Serial Position, and Law of Proximity

Returns a structured audit report with severity-tagged findings (Critical / Warning / Pass), a 0–100 score, and a prioritised action list.

---

## Install

```bash
npx skills add alifnoushad/ux-audit-skill
```

Or copy `SKILL.md` directly into your project and reference it as a system prompt.

---

## Usage

Once installed, invoke in Claude Code or any Claude-powered tool:

```
Audit this interface using the UX audit skill:
[paste URL / screenshot description / Figma summary / component spec]
```

Optional parameters:
```
Focus areas: [navigation / forms / accessibility / conversion / mobile]
Audience context: [B2B / B2C / enterprise / e-commerce / automotive]
```

---

## Example Output

```
## UX Audit Report
Interface: toyota.ae — Vehicle Configurator
Date: 2026-05-18
Overall Score: 71/100 — Adequate

### Critical Findings

Rule 1.3 — Screen Completeness
Severity: Critical
Finding: No error state defined for the finance calculator when monthly payment 
         cannot be computed. Users receive a blank result with no explanation.
Recommendation: Add an inline error state with a plain-language message and 
                a fallback CTA ("Speak to a finance advisor").

Rule 2.8 — WCAG: Keyboard and Focus
Severity: Critical
Finding: The model selector carousel is not keyboard accessible. Tab focus 
         skips past the carousel entirely on desktop.
Recommendation: Implement keyboard navigation on the carousel with 
                arrow key support and visible focus indicators.

### Warnings

Rule 2.2 — Goal-Gradient Effect
Severity: Warning
Finding: The 4-step configuration flow has no progress indicator. Users 
         cannot tell how far they are from completion.
Recommendation: Add a step indicator (Step 2 of 4) with completed 
                steps visually distinct from remaining steps.

### Score Breakdown
Tier 1: 28/39
Tier 2: 21/30
Tier 3: 7.5/10.5 (preview rules only)
Normalised Total: 71/100

### Priority Action List
1. Add error state to finance calculator (Critical — Tier 1)
2. Fix keyboard accessibility on model carousel (Critical — WCAG 2.1)
3. Add progress indicator to configuration flow (Warning — Tier 2)
```

---

## Rule Coverage

### Tier 1 — Structural Rules (13 rules)
Rules that fire on every audit. Auto-checkable.

| Rule | Source |
|---|---|
| 1.1 Visual Consistency | Nielsen #4 |
| 1.2 Component Discipline | Nielsen #4 + delivery observation |
| 1.3 Screen Completeness | Nielsen #9 |
| 1.4 Navigation Logic | Nielsen #3 |
| 1.5 CTA Clarity | Nielsen #8 + Fitts's Law |
| 1.6 Accessibility Baseline | WCAG 2.1 AA |
| 1.7 Content Hierarchy | Nielsen #8 |
| 1.8 Form Usability | Nielsen #6 + #9 |
| 1.9 Decision Simplicity | Hick's Law |
| 1.10 Cognitive Load | Miller's Law |
| 1.11 Familiar Patterns | Jakob's Law |
| 1.12 Input Tolerance | Postel's Law |
| 1.13 Responsive Layout | WCAG 2.1 SC 1.4.10 |

### Tier 2 — Heuristic, Behavioural, and WCAG Rules (15 rules)
Rules requiring AI judgment. Apply to every audit.

| Rule | Source |
|---|---|
| 2.1 Peak-End Rule | Kahneman |
| 2.2 Goal-Gradient Effect | Behavioural psychology |
| 2.3 Von Restorff Effect | Gestalt |
| 2.4 Aesthetic-Usability Effect | Norman |
| 2.5 Serial Position Effect | Memory research |
| 2.6 Law of Proximity | Gestalt |
| 2.7 WCAG: Perceivable | WCAG 2.1 Principle 1 |
| 2.8 WCAG: Operable | WCAG 2.1 Principle 2 |
| 2.9 WCAG: Understandable | WCAG 2.1 Principle 3 |
| 2.10 WCAG: Robust | WCAG 2.1/2.2 Principle 4 |
| 2.11 WCAG 2.2 Target Size | WCAG 2.2 SC 2.5.8 |
| 2.12 Feedback and System Status | Nielsen #1 |
| 2.13 Error Prevention and Recovery | Nielsen #5 + #9 |
| 2.14 Help and Documentation | Nielsen #10 |
| 2.15 Trust and Safety Signals | Nielsen #2 + delivery |

### Tier 3 — Experience Quality Rules (7 rules — preview)
Proprietary rules from IBM iX enterprise delivery. Full rules available in the UX Intelligence Engine.

- 3.1 JTBD Alignment
- 3.2 Journey Narrative Coherence
- 3.3 Brand-Experience Alignment
- 3.4 AI Feature Value Assessment
- 3.5 Conversion Architecture
- 3.6 Emotional Resonance
- 3.7 Dashboard and Data Storytelling

---

## Want the Full Tier 3 + AI-Powered Audit Engine?

The **UX Intelligence Engine** runs all 35 rules automatically against any interface.

- Scored PDF audit reports
- AI-powered findings with evidence-based recommendations
- WCAG compliance summary
- Prioritised fix queue
- Built for UX teams, product managers, and design consultancies

**[→ UX Intelligence Engine](#)** *(link coming soon)*

---

## About

**Alif Noushad** is a Senior Experience Designer at IBM iX Studio Dubai with 6+ years of experience in UX strategy, service design, AI-enabled design, and enterprise product design.

This skill distils the audit framework used across enterprise engagements for Toyota UAE, Lexus UAE, Al Ghurair Properties, and other Al-Futtaim clients.

- Portfolio: [alifnoushad.com](https://alifnoushad.com)
- LinkedIn: [linkedin.com/in/alifnoushad](#)

---

## License

Tier 1 and Tier 2 rules are open and free to use. Tier 3 rules are proprietary — preview descriptions are included here; full weighted rules are available in the UX Intelligence Engine.

MIT License — Tier 1 and Tier 2 only.
