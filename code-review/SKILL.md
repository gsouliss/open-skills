---
name: code-review
description: Perform a comprehensive code review focusing on correctness, performance, readability, and security.
version: 1.0.0
author: Your Name
triggers:
  - type: keyword
    patterns:
      - "review this code"
      - "check this pull request"
      - "code review"
---

## Code Review Checklist

1. **Correctness**
   - Does the code implement the intended functionality?
   - Are edge cases handled?
   - Are there potential bugs or infinite loops?

2. **Performance**
   - Are there inefficient algorithms (e.g., nested loops, redundant calls)?
   - Is memory usage optimized?

3. **Readability & Maintainability**
   - Are variable and function names descriptive?
   - Is the code well-commented where necessary?
   - Is there consistent formatting?

4. **Security**
   - Are there injection risks (e.g., SQL, XSS)?
   - Are secrets or credentials exposed?
   - Are input validations sufficient?

5. **Best Practices**
   - Follows project’s coding standards.
   - Uses appropriate design patterns.
   - Includes tests for new logic.

## Example Usage
> "Review this pull request for the login module."

## Instructions
When triggered, analyze the provided code changes line-by-line, reference the checklist above, and return a structured review with:
- Summary of key issues
- Specific line numbers and suggestions
- Priority levels (High/Medium/Low)
- Recommendations for improvements   
```
- Opencode SKILLS.ms file locations

```
Place files
Create one folder per skill name and put a SKILL.md inside it. OpenCode searches these locations:

Project config: .opencode/skills/<name>/SKILL.md
Global config: ~/.config/opencode/skills/<name>/SKILL.md
Project Claude-compatible: .claude/skills/<name>/SKILL.md
Global Claude-compatible: ~/.claude/skills/<name>/SKILL.md
Project agent-compatible: .agents/skills/<name>/SKILL.md
Global agent-compatible: ~/.agents/skills/<name>/SKILL.md
```

Opencode skills format:

```
---
name: git-release
description: Create consistent releases and changelogs
license: MIT
compatibility: opencode
metadata:
  audience: maintainers
  workflow: github
---

## What I do

- Draft release notes from merged PRs
- Propose a version bump
- Provide a copy-pasteable `gh release create` command

## When to use me

Use this when you are preparing a tagged release.
Ask clarifying questions if the target versioning scheme is unclear.