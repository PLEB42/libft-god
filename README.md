# Libft-God (2026 Edition) 🚀

**Libft-God** is an advanced, high-performance tester for the 42 school `libft` project. It is designed to ensure your library fully complies with the 2026 PDF standards, offering rigorous functional testing, memory leak detection, and style checks.

## ✨ Features

- ✅ **Comprehensive Functional Testing:** Covers Part 1, Part 2, Bonus (Part 3), and additional extra functions.
- ⚡ **Turbo Mode:** Features a `-fast` flag for optimized, one-shot memory leak detection, drastically reducing test execution time.
- 🍎🐧 **Cross-Platform Memory Checks:** Automatically uses **Valgrind** on Linux and native **Leaks** on macOS to verify memory safety.
- 🎨 **Modern Interface:** Displays results in a clean, color-coded table format with real-time progress tracking.
- 📏 **Norminette Integration:** Performs syntax and norm checks directly via the script.
- 🚫 **Forbidden Functions:** Automatically scans your binaries to ensure no unauthorized functions are used.
- 🛠️ **Makefile Validation:** Rigorously tests all mandatory rules (`all`, `clean`, `fclean`, `re`).
- 🎯 **Granular Testing:** Allows you to test specific functions or isolated parts of the project.

## 📋 Prerequisites

To use this tester, you will need:
- **Norminette** (installed in your environment).
- **Valgrind** (required on Linux for leak detection).
- **CC** compiler.

## 🚀 How to Use

### 1. Configuration

Before running the tester, you must configure the path to your `libft` project.

1. Create your configuration file from the template:
   ```bash
   cp srcs/config_template.sh my_config.sh
   ```
2. Edit `my_config.sh` and set the `PATH_LIBFT` variable to the absolute or relative path of your project:
   ```bash
   PATH_LIBFT="/path/to/your/libft"
   ```

### 2. Execution

To run the standard test suite:
```bash
bash grademe.sh
```

### 3. Useful Commands & Examples

- **Test a single function:**
  ```bash
  bash grademe.sh ft_atoi
  ```

- **Run in Fast Mode (Optimized Leak Check):**
  ```bash
  bash grademe.sh -fast
  ```

- **Test a specific part:**
  ```bash
  bash grademe.sh -op1  # Only Part 1
  bash grademe.sh -op2  # Only Part 2
  bash grademe.sh -op3  # Only Bonus (Part 3)
  ```

- **Skip specific checks:**
  ```bash
  bash grademe.sh -n    # Skip Norminette checks
  bash grademe.sh -f    # Skip forbidden functions check
  ```

## 🛠️ Available Options

| Flag | Description |
| :--- | :--- |
| `-h`, `--help` | Displays the full manual. |
| `-a`, `--about` | Displays the About page and Pleb_42 organization credits. |
| `-fast` | Enables fast mode (one-shot memory leak checking per function). |
| `-d` | Allows testing even if files are in subdirectories. |
| `-c` | Disables terminal colors. |
| `-m` | Rigorously tests all Makefile rules. |
| `-u` | Disables startup update checks. |
| `-n` | Disables Norminette checks. |
| `-f` | Disables forbidden function checks. |
| `-p1, -p2, -p3` | Disables testing for Part 1, 2, or 3 respectively. |

## 📁 Supported Functions

The tester supports all standard `libc` functions, Part 2 string manipulation functions, linked list functions (Bonus), and various extra functions (e.g., `ft_isspace`, `ft_itoa_base`). Please refer to `supported_functions.md` for the complete list.

## 📜 Credits and History

This project was built upon and inspired by the **libft-war-machine** version maintained by **@0x050f**, which in turn was based on the versions by **@lmartin** and the original **Libftest** created by **@jtoty**. 

The **Libft God** iteration introduces several major improvements, including significant performance optimizations (Fast Mode), updated compatibility with the 42 standards (2026 PDF), and robust, cross-platform memory leak detection for both macOS and Linux.

---
*Disclaimer: This tester is a helpful tool, but passing all tests here does not guarantee a perfect grade. Always double-check your code!*
