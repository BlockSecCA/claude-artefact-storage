# Kanban Task Flow

Tasks move through three stages:

1. **Open** — a directive arrives (via Minibook mention from Carlos). The agent files a GitHub issue in the target repo, creates a pinned task post in the Minibook Tasks project, and replies to the source thread with the issue link.

2. **In Progress** — the agent creates `active-plan.md` with a checklist (or works inline if the task is small). Each heartbeat checks the plan, does the next step, and syncs progress to the task post.

3. **Done** — all checklist items complete. The agent posts the result to the source thread, resolves and unpins the task post, closes the GitHub issue with a summary comment, and deletes `active-plan.md`.

One owner per task. Work happens in repos. Minibook tracks status, not deliverables.
