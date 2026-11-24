---
name: intent-to-evals
description: Use when the user can describe what they want but success is still subjective. Clarify the intended outcome through examples, then turn it into repeatable checks an agent can use to improve its work.
---

# Intentivals

The user may recognize a good result before they can explain what makes it good.
Learn which differences matter to them and why. Turn that understanding into
checks that still work when the next result looks different from the examples.

## Clarify the vision

Start with the request. Describe who will use the result, in what situation,
and what success would look like in use. Use an existing version if one is
available. For a new idea, sketch a small example of the experience.

When two plausible readings would change what you build or how you judge it,
show the user the smallest example that makes the difference visible. Ask
which is closer and why. Leave room for the user to reject both or combine them.

When feedback like “too long” could mean either “cut the detail” or “help me
find the point sooner,” show both edits of the same passage and ask which is
closer and why.

State what you learned in the user's terms. If you're unsure whether the
preference generalizes, predict what the user would prefer in a different
example and ask what you missed. Stop asking when the remaining uncertainty
would leave both the work and its checks unchanged.

## Design the checks

For each distinction that matters, ask what evidence would let a fresh
evaluator recognize it.

- For a fact or constraint, use code and an answer key derived from the source.
- For an ability, give the intended user or a fresh agent a realistic task
  and observe whether they succeed under the conditions that matter.
- For a preference, use a blind comparison. Let the evaluator return a tie.
  Check whether its choices agree with the user's on fresh examples.

Choose the simplest check that captures the intent. Explain why its result
matters. Specify its inputs, procedure, grading rule, and what a failure
should show the agent. Identify which failures outweigh an otherwise better
score. Keep distinct preferences separate while their tradeoff is unresolved.

## Verify the checks

Run each check on an example the user accepts and on a plausible near miss.
Try to produce something the check rewards that the user would reject.
Use any disagreement to refine the check or clarify the intended outcome.
Keep a criterion under human review while its automated check is unreliable.

## Improve against a stable target

Save the agreed intent, runnable checks or evaluator prompts, and the rule
for keeping a revision. Use the existing version as the baseline when one
exists. For new work, use the first candidate.

After each revision, run the same checks under the same conditions. Report
what improved, what regressed, and a concrete failure to guide the next edit.
For variable scores, measure normal variation before treating a gain as real.
Use fresh cases to confirm a candidate and the agreed rule to keep or reject it.

If the user's vision changes or a check proves misleading, update the check
and re-evaluate the baseline before comparing revisions again.
