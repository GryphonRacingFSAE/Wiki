# Gryphon Racing Wiki
A wiki of setups, known issues, workarounds, etc.

## Coding Standards

### Branches

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

### Naming

#### C++
```C++
namespace PascalCase {}
class PascalCase {};
int camelCase() {};
int snake_case = 0;
```

#### TypeScript
```TypeScript
class CamelCase {};
function camelCase {}
let cancelCase: int = 0;
```

### Formatting

#### C & C++

Formatting is handled by clang format.
```bash
find ./src -iname *.hpp -o -iname *.cpp | xargs clang-format -i # In the root folder of the repo.
```

#### TypeScript

All formatting is handled by eslint + prettier. To find the proper eslint and prettier formatting configuration files, see: https://github.com/GryphonRacingFSAE/Discord-Bot
