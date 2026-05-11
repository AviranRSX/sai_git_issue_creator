# Git Issue Creator

This repo helps the algo team create clear GitHub issues from templates.

## How to use

1. Open your LLM tool in this repo.
2. Ask it to use `llm-instructions/github-issue-helper.md`.
3. Describe the task in simple words.
4. Answer any missing questions.
5. Copy the printed issue text into GitHub Issues.

Example:

```text
Use llm-instructions/github-issue-helper.md.
Create a GitHub issue for testing a new radar config on route X.
Due date: 2026-05-20.
Output: run summary with pass/fail result.
Close when: results are reviewed by the algo lead.
```

## Rules

- Use short and simple words.
- Use one template from `templates/`.
- Use `Experiment Plan.md` when planning a field, lab, recording, calibration, detection, tracking, dataset, or validation experiment.
- Always print a short title.
- Always include a calendar date.
- Always include the issue output.
- Always include what closes the issue.
- Use only one checklist, except experiment plans may use `Equipment Checklist` and `Tech Checklist`.
- Ask for side notes or considerations.
- Classify the issue by the templates.
- If no template fits, suggest the closest one.
- If any of these are missing, ask before writing the issue.
