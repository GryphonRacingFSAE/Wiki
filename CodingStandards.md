# Coding Standards

These are a list of language-agnostic standards that Gryphon Racing expects it's members and external contributors to follow. To both reduce friction, and to improve uniformity.

## Branches

- Name your branch as follows: `firstname/branchtopic`, ex. `dallas/move-from-previous-repo`
- `main` is a protected branch, and thus needs a PR to approve merging with it.

### Commits

Do your best to follow this commit message format: [Semantic Commit Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716) by Josh Buchea

#### Example:

```
feat: add hat wobble
^--^  ^------------^
|     |
|     +-> Summary in present tense.
|
+-------> Type: chore, docs, feat, fix, refactor, style, or test.
```

#### List of types and purposes

- `feat`: (new feature for the user, not a new feature for build script)
- `fix`: (bug fix for the user, not a fix to a build script)
- `refactor`: (refactoring production code, eg. renaming a variable)
- `docs`: (changes to the documentation; no production code change)
- `style`: (formatting, missing semi colons, etc; no production code change)
- `test`: (adding missing tests, refactoring tests; no production code change)
- `chore`: (updating grunt tasks etc; no production code change)
- `ci`: (updating ci to change deployment, etc; no production code change)
