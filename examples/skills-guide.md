# Creating Advanced Skills

To create a "Skill" in Claude Code, you simply need to define a repeatable workflow. 

### Example: The "Doc Fixer" Skill
**Prompt:**
"Claude, I want to create a skill called 'doc-fixer'. Whenever I call it, look for all .md files in the current directory, check for broken links, and fix any spelling errors using standard UK English."

### Example: The "PR Reviewer" Skill
**Prompt:**
"Create a skill called 'review-pr'. It should look at the current git diff against main, check for any security vulnerabilities in the changed code, and ensure that all new functions have corresponding test cases in the tests/ folder."
