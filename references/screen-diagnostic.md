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
6. Include before/after comments for the priority fixes: what the current screen makes users think or do, and what the improved version should make easier.
7. Explicitly name the product psychology theories used in the diagnosis and connect each theory to the screen evidence.
8. When the user asks for references, search the web for 2-4 comparable UI patterns, teardown examples, or product pages and explain what to borrow from each.
9. Avoid pretending to know analytics, user intent, or business context not visible in the screenshot.
10. When the user asks for feedback directly on the screenshot, produce a visual annotation artifact in addition to the written diagnosis.

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

3. Name the applied product psychology lens.
   - Include 3-5 theories actually used in the diagnosis.
   - Prefer B.I.A.S, BMAP Ability, BMAP Prompt, Peak-End, cognitive load, information scent, visual hierarchy, loss aversion, social proof, progressive disclosure, feedback loops, or ethical design.
   - For each theory, explain how it appears in the screen in one sentence.
   - Do not list theories that are not used in the findings.

4. Create sticky-note findings.
   - Aim for 5-8 findings.
   - Each finding must be short enough to fit on a visual annotation.
   - Use this shape:
     - `CODE - Short label`
     - `Observed:` visible evidence
     - `Theory:` named product psychology principle
     - `Psychology:` why that principle matters for comprehension/action
     - `Fix:` concrete direction

5. Pick the top 3 fixes.
   - Rank by impact on comprehension/action, not by visual taste.
   - Include expected total score delta if fixed.
   - Add a brief before/after comment for each fix.

6. Provide an after-state brief.
   - Do not generate a full redesign unless asked.
   - Describe the target screen in 4-6 bullets: headline, primary action, layout order, copy change, friction removal, reward signal.

7. Add references when requested.
   - Use web search for current public references rather than inventing examples.
   - Prefer references that match the surface type: landing page, onboarding, pricing, dashboard, checkout, mobile app, or empty state.
   - For each reference, include the source URL and one short "borrow this" note.
   - Do not over-quote source pages; summarize the pattern in your own words.

8. Ask for the next artifact only if needed.
   - If the user wants a redesign, ask for brand constraints or proceed with conservative assumptions if low risk.

## Visual Annotation Mode

Use this mode when the user asks to put feedback on top of the screenshot, mark the screenshot visually, annotate the screen, make sticky notes on the image, or provide a visual critique.

Create an annotated screenshot artifact when the runtime can render or export images. Prefer deterministic overlays over generative redraws:

1. Preserve the original screenshot as the base image.
2. Add numbered pins at the exact visible UI regions being discussed.
3. Add translucent highlight boxes around the affected areas.
4. Add compact margin notes or callout cards that map each number to:
   - short issue label
   - severity
   - theory
   - fix direction
5. Keep the annotated image readable at chat preview size.
6. Put only 3-6 high-signal annotations on the image; keep the full written diagnosis below or in a separate report.
7. Use color consistently:
   - Red: high-impact fix or action blocker
   - Amber: decision/comprehension friction
   - Blue: hierarchy/control clarity issue
   - Green: good pattern to preserve
8. Do not cover the UI region with long text. Put long explanations in the written report.
9. If image rendering is not available, provide a text-only annotation map with approximate regions, for example `#1 top-right studio cards`, `#2 left source list`, `#3 bottom input`.

Recommended visual output shape:

```markdown
## Visual Annotation
[Attach annotated screenshot PNG/SVG/HTML capture]

## Fix First
1. `#1` [Fix] - Expected delta: +N.
2. `#2` [Fix] - Expected delta: +N.
3. `#3` [Fix] - Expected delta: +N.

## Annotation Map
| # | Region | Issue | Theory | Fix |
|---:|---|---|---|---|
| 1 | [visible area] | [short label] | [theory] | [fix direction] |
```

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

## Product Psychology Lens
- **[Theory name]**: [How this screen triggers, violates, or can use the principle].
- **[Theory name]**: ...

## Sticky Notes
1. `FOC - [short issue]`
   Observed: ...
   Theory: ...
   Psychology: ...
   Fix: ...

2. `HIE - [short issue]`
   Observed: ...
   Theory: ...
   Psychology: ...
   Fix: ...

## Fix First
1. [Fix] - because [reason]. Expected total score delta: +N.
   Before: [what the current screen likely makes users think/do].
   After: [what the improved screen should clarify or enable].
2. [Fix] - because [reason]. Expected total score delta: +N.
   Before: ...
   After: ...
3. [Fix] - because [reason]. Expected total score delta: +N.
   Before: ...
   After: ...

## After-State Brief
- ...

## References
- [Reference name](URL) - Borrow this: [specific pattern or decision].
```

## Visual Annotation Template

Use this shorter shape when the deliverable is an annotated image:

```markdown
## Visual Result
[Annotated screenshot attached.]

## Fix First
1. `#1` [highest-impact fix]. Expected total score delta: +N.
   Before: ...
   After: ...
2. `#2` ...
3. `#3` ...

## Reading The Image
- Red callouts are immediate action blockers.
- Amber callouts are comprehension or decision-friction issues.
- Blue callouts are hierarchy/control clarity issues.
- Green callouts are good patterns worth preserving.
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

## Product Psychology Lens
- **B.I.A.S - Block**: Similar-looking choices fail the user's attention filter because there is no recommended starting point.
- **BMAP - Ability**: The screen asks users to choose before lowering decision effort or explaining consequences.
- **Peak-End**: There is no early payoff preview, so the setup step feels like work before reward.

## Sticky Notes
1. `FOC - Primary path is hidden`
   Observed: All setup options have similar size and emphasis.
   Theory: B.I.A.S - Block
   Psychology: The screen fails the Block filter because nothing tells the user where to look first.
   Fix: Recommend one default path and visually mark it as the best starting point.

2. `CPY - CTA lacks outcome`
   Observed: The button says "Continue" instead of naming what happens next.
   Theory: B.I.A.S - Interpret
   Psychology: Weak Interpret clarity makes the click feel uncertain.
   Fix: Change to "Create workspace" or "Import team" depending on the selected path.

3. `RWD - No payoff preview`
   Observed: The page asks for a setup decision but does not show the result.
   Theory: Peak-End + BMAP Motivation
   Psychology: Users see work before reward, which weakens motivation.
   Fix: Add a small preview or progress note: "You will get a ready-to-use dashboard in 2 minutes."

## Fix First
1. Make one path the recommended default - because it reduces decision effort. Expected total score delta: +3.
   Before: Users must compare equal-looking options and guess which one is safest.
   After: Users see a recommended path and can start without overthinking.
2. Rewrite CTA copy around the next outcome - because it increases action confidence. Expected total score delta: +2.
   Before: "Continue" hides the consequence of the click.
   After: The CTA names the next outcome, so the click feels safer.
3. Add a payoff preview - because it turns setup effort into visible progress. Expected total score delta: +2.
   Before: The screen asks for work before showing what users get.
   After: A preview or progress note makes the reward visible before commitment.

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

If the user asks for references:

- Search the web before answering.
- Keep references subordinate to the diagnosis; they support the recommendation, not replace it.
- Use reference examples to justify concrete screen decisions such as CTA hierarchy, social proof placement, pricing comparison, onboarding step order, or progress/payoff signals.
