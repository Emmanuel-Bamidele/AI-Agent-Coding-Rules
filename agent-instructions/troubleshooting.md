# Troubleshooting Guide for Agents

## If tests fail

1. Read the failure.
2. Determine whether the test or code is wrong.
3. Do not delete the test just to pass.
4. Fix root cause.
5. If unrelated, report it clearly.

## If lint fails

1. Fix the lint issue if related.
2. Avoid disabling the rule.
3. If disabling is necessary, explain why inline or in final response.

## If type checks fail

1. Prefer precise types.
2. Avoid `any`.
3. Avoid unsafe casts.
4. Do not suppress errors unless unavoidable and justified.

## If build fails

1. Capture the command and error.
2. Identify whether the failure is caused by your change.
3. Fix if related.
4. Report if unrelated.

## If requirements are unclear

Do not invent behavior.

Prefer:

- Inspect existing behavior
- Preserve compatibility
- Add a note about ambiguity
- Make the smallest reversible change

## If a change becomes too large

Stop and split the work.

Report:

- What was discovered
- Why the scope expanded
- Recommended smaller steps
