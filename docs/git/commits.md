# Git commits

## Commit message

### 1. Separate subject from body with a blank line
It’s a good idea to begin the commit message with a single short (less than 50 character) line summarizing the change, followed by a blank line and then a more thorough description (not mandatory).

```
Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary.
```

You can use `git log --oneline` or `git shortlog` to see only messages' subject.

### 2. Limit the subject line to 50 characters

### 3. Capitalize the subject line

### 4. Do not end the subject line with a period

### 5. Use the imperative mood in the subject line
Spoken or written as if giving a command or instruction.
A properly formed Git commit subject line should always be able to complete the following sentence:

`If applied, this commit will <your subject line here>`

### 6. Wrap the body at 72 characters
Max 72 characters per line

### 7. Use the body to explain what and why vs. how

### 8. Add type to subject
`{{TYPE}}: {{Subject}} (Maks 50 characters)`
- feat - feature, new functionality
- fix - bug fix, not adding anything new, but rather removing "unwanted feature".
- refactor - refactoring of production code. This type of commit should not have an impact on end-user experience at any point. The application's behavior should remain the same, and only the refactoring is applied.
- style - code style improvements, without any changes in the app's behavior
- doc - documentation changes. That include README updates and any other documentation-specific things.
- test - test coverage improvements
- chore - changes which do not affect the application behavior, like .gitignore, grunt files, etc, configuration, performance improvements and so on.

## Good practise for commits

- Commit early, commit often
- Don’t commit generated files
- Squash redundant commits
- Better WIP commit than stash
