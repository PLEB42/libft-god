# Changes Log - Libft-God (2026 Edition)

## [2026-06-06] - No-Makefile Mode & Skip Mechanism

### Added
- **No-Makefile Mode (`-M` flag)**: 
  - Allows testing functions by compiling individual `.c` files directly with the test mains.
  - Useful for situations where one function doesn't compile and prevents the generation of `libft.a`.
  - Automatically sets `OPT_NO_LIBRARY=1` and `OPT_NO_MAKEFILE=1`.
- **New Variable**: `OPT_NO_MAKEFILE` added to `srcs/variables.sh` to track the state of the new mode.
- **Documentation**: Added `-M` flag description to the `help.1` manual.

### Modified
- **`grademe.sh`**:
  - Implemented logic to parse the `-M` flag.
  - Enhanced activation loops to detect and skip functions prefixed with `#` in the function arrays.
- **`srcs/check_compilation.sh`**:
  - Updated the `compilation` function to check for `OPT_NO_MAKEFILE`.
  - If active, it links the `.c` file directly instead of using `libft.a`.
- **`srcs/check_cheat.sh`**:
  - Updated `check_cheating` to support direct file checking without requiring `libft.a` when in No-Makefile mode.
  - Improved path resolution for bonus vs non-bonus files.

### Fixed
- Issue where a single non-compiling function would block the entire tester by failing the library build.
