# GitHub Issue Helper

Create GitHub issue text for the algo team.

Use short and simple words.

## Input Check

Before writing the issue, make sure you have:

- Task type.
- Clear task goal.
- Calendar due date, such as `2026-05-20`.
- Expected output.
- What closes the issue.
- Dependencies, if any.
- Blocked issues, if any.
- Side notes, if any.

For an experiment plan issue, also make sure you have:

- Experiment goal.
- Experiment location.
- Equipment checklist.
- Tech checklist and what must be confirmed before the experiment.
- Schedule.
- Planned scenes or experiment blocks.
- Time estimate for every scene or block.

If the due date is missing, ask:

```text
What is the calendar due date for this work?
```

If the expected output is missing, ask:

```text
What should this issue output?
```

If the close condition is missing, ask:

```text
What must be true to close this issue?
```

Always check for dependencies.

If the task may depend on another GitHub issue, ask:

```text
Does this depend on another GitHub issue? If yes, what is the issue number, such as #123?
```

Always check if this issue can block another GitHub issue.

Ask:

```text
Can this block another GitHub issue? If yes, what is the issue number, such as #123?
```

Always ask:

```text
Are there any side notes or considerations for this issue?
```

Do not guess missing facts.

## Classify Issue

Use one file from `templates/`:

- `Feature Task.md`: new behavior or new capability.
- `Bug Fix Task.md`: broken behavior.
- `Research Task.md`: question, study, spike, or analysis.
- `Experiment Plan.md`: plan a field, lab, recording, calibration, detection, tracking, dataset, or validation experiment.
- `Run Task.md`: run a job, config, model, script, or data flow.
- `Infra Task.md`: infra, deployment, scale, alerts, permissions, or system setup.
- `Ops Task.md`: admin or team operation.
- `Tech Debt.md`: refactor, cleanup, weak code, old code, or risk.
- `Documentation Task.md`: docs, README, wiki, guide, or examples.

First classify the issue type from this list.

Use `Experiment Plan.md` when the user asks to plan an experiment, even if the experiment includes research, calibration, validation, or data recording.

If more than one template fits, pick the most direct one.

If no template fits, do not force it. Suggest the closest template and ask the user if they want to use it.

## Write Rules

- Keep every sentence short.
- Use bullets where possible.
- Keep only useful details.
- Do not add long background.
- Keep the emoji symbols in section headers from the selected template.
- Use emoji symbols in added section headers too.
- Use this style for added sections:
  - `## 📦 Output`
  - `## ✅ Close Criteria`
  - `## 🔄 Dependencies`
  - `## 🧱 Checklist`
  - `## 🧠 Side Notes`
- Do not invent owners, dates, links, issue IDs, or metrics.
- If a field is unknown and not required, write `N/A`.
- Always print a short title.
- Use exact calendar dates. Do not write only `ASAP`, `next week`, or `soon`.
- Include a `## 📦 Output` section, even if the template does not have one.
- Include a `## ✅ Close Criteria` section, even if the template does not have one.
- Include a `## 🔄 Dependencies` section, even if the template does not have one.
- In `Dependencies`, include `Depends on` and `Blocks`.
- Use GitHub issue numbers with `#`, such as `#123`.
- If there are no dependencies, write `Depends on: N/A`.
- If this does not block another issue, write `Blocks: N/A`.
- For non-experiment issues, use only one checklist in the whole issue.
- For non-experiment issues, put all checkbox items under one section named `## 🧱 Checklist`.
- For non-experiment issues, do not use checkboxes in other sections.
- Put notes and considerations in one section named `## 🧠 Side Notes`.
- Keep GitHub checkbox syntax: `- [ ]`.

For experiment plan issues:

- Include a section named `## 🎯 Experiment Goal`.
- Include a section named `## 📍 Location`.
- Include a section named `## 🎒 Equipment Checklist`.
- Include a section named `## 🧱 Tech Checklist`.
- Include a section named `## 🧪 Experiment Plan`.
- Include a section named `## ⏳ Schedule`.
- Each planned scene or block must include a time estimate.
- Use checkboxes only in `Equipment Checklist` and `Tech Checklist`.
- Do not add a third checklist section.

## Output Format

Print only two copy-paste blocks.

First print the GitHub issue title:

```text
Title:
<short issue title>
```

Then print the GitHub issue body as Markdown:

```markdown
<filled issue body>
```

Do not explain your choices after the issue.

## Quality Bar

The issue is ready only when a team member can answer:

- What work should be done?
- Why is it needed?
- What date matters?
- What should be produced?
- What closes the issue?
- How will it be checked?
