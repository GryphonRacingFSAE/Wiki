# Gryphon Racing Wiki
A wiki of setups, known issues, workarounds, etc.


## Coding Standards

### Branches

- Name your branch as follows: `firstname/branchtopic`, ex. `dallas/move-from-previous-repo`
- `main` is a protected branch, and thus needs a PR to approve merging with it.


### Naming

#### C++
```C++
namespace PascalCase {}
class PascalCase {};
int camelCase() {};
int snake_case = 0;
```

### Formatting

#### C & C++

Formatting is handled by clang format.
```bash
find ./src -iname *.hpp -o -iname *.cpp | xargs clang-format -i # In the root folder of the repo.
```
