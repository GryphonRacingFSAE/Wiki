# Style Guide

## Naming

### C & C++
```C++
#define SCREAMING_SNAKE_CASE
namespace PascalCase {}
class PascalCase {};
int camelCase() {};
int snake_case = 0;
```

### CMake
```CMake
set(SCREAMING_SNAKE_CASE)
```

### Javascript/TypeScript
```TypeScript
class PascalCase {};
interface PascalCase {};
type PascalCase = {
    snake_case: number;
};
function camelCase(snake_case: number) {}
let snake_case: number = 0;

// Prefer:
function myFunction() {}
// Instead of:
const myFunction = () => {};
```

### Python
```python
class PascalCase:
def snake_case(snake_case):
snake_case = 0
```

### Rust
```rust
struct PascalCase {};
enum PascalCase {
    PascalCase1,
    PascalCase2
};
trait PascalCase {};
fn snake_case(snake_case: PascalCase) -> PascalCase {
	return snake_case; // Explicit returns only
};
let snake_case: PascalCase = ...;
```

## Formatting

### C & C++

Formatting is handled by [clang-format](https://clang.llvm.org/docs/ClangFormat.html). The configuration file (.clang-format) can be found [here](./style/.clang-format).
Most editors have clang-format integrated.

To run clang-format command line (Linux only):
```bash
find . -name "*.hpp" -o -name "*.cpp" | xargs clang-format -i # In the root folder of the repo.
```

### CMake

Formatting is handled by [cmake-format](https://github.com/cheshirekow/cmake_format). The configuration file (.cmake-format.yaml) can be found [here](./style/.cmake-format.yaml). The majority of editors don't have cmake-format integrated, but there are extensions available.

To run cmake-format command line (Linux only):
```bash
find . -name "CMakeLists.txt" -o -name "*.cmake" | xargs -n 1 cmake-format -i # In the root folder of the repo.
```

### Javascript/TypeScript

All formatting is handled by [eslint](https://eslint.org/) + [prettier](https://prettier.io/). The configuration files (.eslintrc.cjs) and (.prettierrc.json) can be found [here](./style/.eslintrc.cjs) and [here](./style/.prettierrc.json) respectively.

To run eslint/prettier command line:
```bash
eslint . --ext .vue,.js,.jsx,.cjs,.mjs,.ts,.tsx,.cts,.mts --ignore-path .gitignore --fix
```


### Python

Formatting is handled by [black](https://github.com/psf/black). The configuration file (pyproject.toml) can be found [here](./style/pyproject.toml). A large number of editors have black integrated or available as an extension.

To run black command line:
```bash
black .
```


### Rust
All formatting should be handled by [rustfmt](https://github.com/rust-lang/rustfmt). Formatting file can be found [here](./style/rustfmt.toml)
Running this command will apply formatting onto the working directory:
```rust
cargo fmt
```
