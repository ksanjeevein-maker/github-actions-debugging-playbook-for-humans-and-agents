# GitHub Actions Debugging Playbook for Humans and Agents Review Checklist

Use this checklist during code review, design review, or migration planning.

- Is the workflow being debugged in the correct event context?
- Are shell, path, and OS assumptions visible and accurate?
- Do cache keys reflect real dependency invalidation inputs?
- Are permissions and secrets appropriate for the job?
- Will the next failure produce better evidence than the current one?
