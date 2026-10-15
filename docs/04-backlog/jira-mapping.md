# Markdown → Jira Mapping

Use this cheat sheet when retiring and opening the Jira project.

| Markdown | Jira |
|----------|------|
| `docs/03-features/<feature>/` | Epic |
| Feature README summary / goals | Epic description |
| `stories.md` rows | Stories |
| Acceptance criteria in stories | Story AC |
| Checklist / task hints | Sub-tasks |
| `products.md` rows | Linked in story description or Components |
| ADR (`docs/05-decisions/`) | Confluence/link in Epic, or comment |
| Priority `P0`–`P3` | Jira Priority |
| Status `ready` | Ready for sprint refinement |

## Suggested Jira fields / labels

- Labels: `electrical`, `plumbing`, `carpentry`, `exterior`, `safety`
- Components: mirror major systems
- Custom link / field: path to markdown feature folder

## Import order

1. Create epics from feature index
2. Create stories from each `stories.md`
3. Attach ADR links on epics that depend on them
4. Sequence epics using architecture build order
