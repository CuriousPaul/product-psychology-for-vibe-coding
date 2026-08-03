# Screen Diagnostic

Use this reference when the user shares a product UI, landing page, dashboard, onboarding, pricing, checkout, mobile screen, or AI-generated screen and asks for a screenshot critique, UX/UI teardown, hierarchy review, scorecard, sticky-note review, or design judgment training.

This is product psychology applied to visible screens. Produce a diagnosis, not a generic design review.

## Core Contract

The output must be visual, specific, prioritized, and teachable:

1. Identify visible problems from the screenshot.
2. Label each problem with a stable short rubric code.
3. Explain why it hurts user comprehension or action.
4. Give a concrete fix direction.
5. Prioritize the top 3 fixes.
6. Avoid pretending to know analytics, user intent, or business context not visible in the screenshot.

## Five-Dimension Rubric

| Code | Dimension | Question | Psychology bridge |
|---|---|---|---|
| `CPY` | Copy | Are labels, headings, CTAs, and helper text concrete and action-oriented? | Interpret: users must instantly understand value and consequence. |
| `FOC` | Focus | Is the primary action or primary information immediately obvious? | Block: the screen must pass the user's attention filter. |
| `HIE` | Hierarchy | Does the screen guide the eye in the right order? | Block + Interpret: order reduces scanning cost and ambiguity. |
| `FRI` | Friction | Does the UI reduce cognitive, interaction, form, or decision effort? | BMAP Ability + Act: users act when the next step feels easy enough. |
| `RWD` | Reward | Does the screen make the user's payoff, progress, or outcome feel clear? | Store + Peak-End: users remember progress, payoff, and relief. |

Accessibility issues belong under `FRI` when they block use, and under `HIE` when contrast, legibility, or tap-target issues weaken scanning.

## Severity Guide

- High: blocks comprehension, hides the primary action, or creates meaningful trust/action risk.
- Medium: slows decisions or weakens confidence.
- Low: polish issue with limited behavioral impact.

## Scoring Guide

- 5: clear and purposeful; only minor improvements.
- 4: mostly strong; one visible weakness.
- 3: understandable but requires effort.
- 2: repeated visible issues slow action or comprehension.
- 1: confusing, misleading, inaccessible, or action-blocking.

## Expected Delta

Expected delta is the likely total score improvement out of 25 after the fix, not a conversion estimate.

- `+1`: small clarity or polish improvement.
- `+2`: noticeable improvement to one dimension.
- `+3`: major improvement to comprehension, action confidence, or decision speed.
- `+4+`: reserved for fixes that unblock the primary task or repair multiple dimensions.

Use "expected" or "likely"; do not imply measured impact without data.

## Diagnosis Workflow

1. Snapshot the screen in one sentence.
   - Name the surface and likely user job.
   - If context is uncertain, say "looks like" instead of asserting.

2. Score the screen.
   - Score each dimension 1-5.
   - Give total out of 25.
   - Add one sentence explaining the score pattern.

3. Create sticky-note findings.
   - Aim for 5-8 findings.
   - Each finding must be short enough to fit on a visual annotation.
   - Use this shape:
     - `CODE - Short label`
     - `Observed:` visible evidence
     - `Psychology:` B.I.A.S/BMAP/Peak-End reason
     - `Fix:` concrete direction

4. Pick the top 3 fixes.
   - Rank by impact on comprehension/action, not by visual taste.
   - Include expected total score delta if fixed.

5. Provide an after-state brief.
   - Do not generate a full redesign unless asked.
   - Describe the target screen in 4-6 bullets: headline, primary action, layout order, copy change, friction removal, reward signal.

6. Ask for the next artifact only if needed.
   - If the user wants a redesign, ask for brand constraints or proceed with conservative assumptions if low risk.

## Output Template

```markdown
## Snapshot
[One-sentence description of what this screen appears to be doing.]

## Score
| Dimension | Score | Note |
|---|---:|---|
| Copy | /5 |  |
| Focus | /5 |  |
| Hierarchy | /5 |  |
| Friction | /5 |  |
| Reward | /5 |  |
| Total | /25 |  |

## Sticky Notes
1. `FOC - [short issue]`
   Observed: ...
   Psychology: ...
   Fix: ...

2. `HIE - [short issue]`
   Observed: ...
   Psychology: ...
   Fix: ...

## Fix First
1. [Fix] - because [reason]. Expected total score delta: +N.
2. [Fix] - because [reason]. Expected total score delta: +N.
3. [Fix] - because [reason]. Expected total score delta: +N.

## After-State Brief
- ...
```

## Style Rules

- Be direct and specific.
- Prefer concrete UI words: headline, CTA, empty state, navigation, field label, contrast, spacing, density, affordance, grouping, progressive disclosure.
- Keep each sticky-note label under 8 words.
- Do not write a long essay unless the user asks.
- Do not over-index on aesthetics. Explain how issues affect comprehension, trust, completion, or decision speed.
- Do not claim exact conversion impact without data.
- If a screenshot is low-resolution or cropped, state which diagnosis areas are low confidence.

## Example Diagnosis

User asks: "이 화면을 점수화해서 어디부터 고쳐야 할지 알려줘."

Response:

```markdown
## Snapshot
Looks like a SaaS onboarding screen asking users to choose a workspace setup path, but the primary path is not obvious.

## Score
| Dimension | Score | Note |
|---|---:|---|
| Copy | 3/5 | Labels are understandable, but the outcome of each choice is vague. |
| Focus | 2/5 | Multiple buttons compete for attention. |
| Hierarchy | 2/5 | The headline, cards, and helper text have similar weight. |
| Friction | 3/5 | The choice is simple, but users need to infer consequences. |
| Reward | 2/5 | The screen does not preview what users get after choosing. |
| Total | 12/25 | The screen is usable, but weak prioritization makes the first action slower than it should be. |

## Sticky Notes
1. `FOC - Primary path is hidden`
   Observed: All setup options have similar size and emphasis.
   Psychology: The screen fails the Block filter because nothing tells the user where to look first.
   Fix: Recommend one default path and visually mark it as the best starting point.

2. `CPY - CTA lacks outcome`
   Observed: The button says "Continue" instead of naming what happens next.
   Psychology: Weak Interpret clarity makes the click feel uncertain.
   Fix: Change to "Create workspace" or "Import team" depending on the selected path.

3. `RWD - No payoff preview`
   Observed: The page asks for a setup decision but does not show the result.
   Psychology: Users see work before reward, which weakens motivation.
   Fix: Add a small preview or progress note: "You will get a ready-to-use dashboard in 2 minutes."

## Fix First
1. Make one path the recommended default - because it reduces decision effort. Expected total score delta: +3.
2. Rewrite CTA copy around the next outcome - because it increases action confidence. Expected total score delta: +2.
3. Add a payoff preview - because it turns setup effort into visible progress. Expected total score delta: +2.

## After-State Brief
- Headline explains the user goal, not the system task.
- One recommended card is visually dominant.
- CTA changes based on selected option.
- Helper copy explains time, consequence, and reversibility.
- A progress/payoff line shows what the user gets next.
```

## Escalation Paths

If the user asks for a redesign:

- Keep the diagnosis first.
- Then provide a wireframe-level after-state.
- If they ask for an image/mockup, use the appropriate image/design tool and preserve the top 3 fixes as acceptance criteria.

If the user asks to turn diagnosis into product logic:

- Extract findings into structured JSON fields: `dimension`, `code`, `severity`, `evidence`, `psychology`, `fix`, `expected_delta`.
- Use this as a first scoring schema for a future trainer product.
