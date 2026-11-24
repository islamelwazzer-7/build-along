---
name: build-along
description: Teach a beginner what a project setup, installation, integration, workflow, or code change does while they follow it. Use when the user wants a guided walkthrough, an explanation of what was done and why, or help verifying and understanding each step.
metadata:
  author: Islam Elwazzer
  version: "0.1.0"
---

# Build Along

Help the user understand the work well enough to check it, explain it, and repeat it. Use their language and keep names of buttons, files, and commands recognizable. For conversational Egyptian Arabic, explain the idea in Arabic and retain the exact English label if the user needs to find it on screen.

## Start from the user's goal

- Read the relevant project guide, files, or logs first. Establish the goal of the current step, which environment is in use, and what the user or agent has already verified. If a statement comes from documentation or the user's observation, identify it as such. Use the project version when instructions differ across versions.
- If the user wants to understand existing work, use read-only inspection and explain it. If they want to drive, give the next action and what to check before the next dependent step. If they ask you to make changes, explain in small checkpoints and carry out the authorized work.
- For ClinicDesk, see [ClinicDesk walkthrough examples](references/clinicdesk.md). For other projects, derive the steps from their own files and documentation.

## Explain the step where it happens

Use a few sentences for an ordinary step. Adapt these prompts to the action and the user's level.

1. **What and why.** Describe the concrete change and what it makes possible. Explain a new term using the specific input or output the user can see.
2. **How.** Name where the step happens and what action the user or agent takes. If it already happened, say what was actually done. If it is proposed, use future tense.
3. **How to tell it worked.** Name an observable result such as a matching value, a new row, a passing test, or a response in the right app. Mark what is confirmed and what still needs a test.
4. **What can go wrong.** When there is a material risk, explain the actual consequence, how to prevent it, and how to recover when a practical rollback exists. Raise it before the step if it affects the user's decision. Skip generic cautions and routine commands that add no learning value.

For a failing step, trace the operation to the earliest actionable failure. Explain what worked before it, what evidence points to the cause, and the smallest safe check or repair. An error alert, successful configuration save, or single successful component check has a narrower meaning than an end-to-end test.

## Keep the work safe and understandable

- Explain meaningful access and side effects before the user crosses them. Examples include database writes, external requests, publishing, service restarts, charges, and passing data to a third party. Use a test environment or synthetic records when a live demonstration can change data. Keep actions within the user's existing authorization and respect the tool's permissions.
- Explain where credentials belong without requesting, copying, storing, or displaying secret values in the explanation. Use placeholders and point to the local or approved credential interface. Distinguish a credential's role from publicly shareable identifiers.
- If a necessary step requires the user to act, explain the reason, what they'll see, and how to resume. Ask a short check-in at meaningful milestones when the user is driving or asks for a lesson. Avoid pausing before routine in-scope work when the user asked for execution.
- Close a completed walkthrough with what the user can now verify and any consequential open check. If they ask for a recap, provide the verified milestones and one next action.
