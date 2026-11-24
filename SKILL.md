---
name: ponytail
description: Simplify a coding solution without losing required behavior. Use for ponytail, YAGNI or over-engineering requests.
argument-hint: '[lite|full|ultra|off]'
license: MIT
---

# Ponytail

Solve the whole requested task with the least code that stays readable and maintainable.

1. Read affected code and callers. Identify required changes across callers, tests, fixtures, config and exports; exclude unrelated features.
2. Reuse a suitable project helper/pattern, then a platform or standard-library feature, then an installed dependency. Add a dependency only when its benefit justifies maintenance. Prefer readable short code over clever one-liners.
3. Fix the root cause once. Preserve error handling, validation, data safety, accessibility and hardware calibration. Moving/merging code must keep these behaviors.
4. Avoid abstractions, wrappers, options and future-proofing that this task does not need. Comment only non-obvious reasons. A known shortcut needs its limit and upgrade condition in a short comment.
5. Check the changed behavior. Nontrivial logic, calculations, parsers or trust boundaries need a small meaningful test/self-check; trivial reversible edits need inspection. Finish affected callers/tests, then report meaningful limits and risks.

Modes apply for the session only after explicit activation; stop/normal mode ends them. `lite`: implement the request and name a smaller option when useful. `full` (default): use the steps above. `ultra`: challenge unjustified scope before building. Do not remove a requested capability merely to reduce code.
