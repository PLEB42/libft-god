# Supported Functions & Test Cases

This document lists all functions supported by the Libft God Tester (Version 2026), organized by project parts, and the specific edge cases tested for each.

## 1. Part I - Libc Functions

These functions mimic standard C library behavior.

| Function | Edge Cases Tested |
| :--- | :--- |
| `ft_isalpha` | Full ASCII range (0-255), boundary chars ('A', 'Z', 'a', 'z'). |
| `ft_isdigit` | Full ASCII range (0-255), boundary chars ('0', '9'). |
| `ft_isalnum` | Full ASCII range (0-255), mixing digits and letters. |
| `ft_isascii` | Full ASCII range (0-255), testing beyond 127. |
| `ft_isprint` | Full ASCII range (0-255), testing non-printable and space. |
| `ft_strlen` | Empty string (`""`), long strings, special characters. |
| `ft_memset` | Size 0, large memory blocks, filling with `\0` vs other values. |
| `ft_bzero` | Size 0, large memory blocks. |
| `ft_memcpy` | Size 0, large blocks (standard behavior: overlap is undefined). |
| `ft_memmove` | Size 0, **Overlapping memory regions** (src < dst and src > dst). |
| `ft_strlcpy` | Size 0, size smaller than src, size exactly `strlen(src) + 1`. |
| `ft_strlcat` | Size 0, size smaller than existing dst, size exactly `strlen(dst) + strlen(src) + 1`. |
| `ft_toupper` | Full ASCII range, lowercase vs non-lowercase. |
| `ft_tolower` | Full ASCII range, uppercase vs non-uppercase. |
| `ft_strchr` | Search for `\0`, search char not in string, char at start/end. |
| `ft_strrchr` | Search for `\0`, char not found, char appearing multiple times. |
| `ft_strncmp` | Length 0, strings identical up to `n`, empty strings. |
| `ft_memchr` | Search beyond string length (up to `n`), char not found, search for `\0`. |
| `ft_memcmp` | Length 0, differing at the beginning/end of `n`. |
| `ft_strnstr` | Needle longer than haystack, empty needle, length `n` limiting find. |
| `ft_atoi` | INT_MIN/MAX, spaces/tabs, invalid signs, non-numeric chars. |
| `ft_calloc` | 0 elements/size, allocation overflow, zero-initialization check. |
| `ft_strdup` | Empty string, very long string, allocation check. |

## 2. Part II - Additional Functions

Functions that provide extra string and memory utility.

| Function | Edge Cases Tested |
| :--- | :--- |
| `ft_substr` | `start` beyond `strlen`, `len` larger than remaining string, empty string. |
| `ft_strjoin` | Two empty strings, one empty string. |
| `ft_strtrim` | Only trim characters, no trim characters, empty string, all trimmed. |
| `ft_split` | Empty string, no delimiters, only delimiters, delimiters at start/end. |
| `ft_itoa` | `0`, `INT_MIN`, `INT_MAX`, negative/positive numbers. |
| `ft_strmapi` | Empty string, index-based character transformation. |
| `ft_striteri` | Empty string, index-based in-place modification. |
| `ft_putchar_fd` | Standard output (1), Error (2), custom FDs. |
| `ft_putstr_fd` | Empty string, strings with newlines, different FDs. |
| `ft_putendl_fd` | Correct newline append, different FDs. |
| `ft_putnbr_fd` | `0`, `INT_MIN`, `INT_MAX`, negative numbers. |

## 3. Part III - Linked List Functions

Management and manipulation of the `t_list` structure.

| Function | Edge Cases Tested |
| :--- | :--- |
| `ft_lstnew` | NULL content, dynamic allocation check. |
| `ft_lstadd_front`| Adding to empty list, adding to existing list. |
| `ft_lstsize` | Empty list (0), single element, multiple elements. |
| `ft_lstlast` | Empty list (NULL), single element, multiple elements. |
| `ft_lstadd_back` | Adding to empty list, adding to existing list. |
| `ft_lstdelone` | Deleting single node, handling the `del` function. |
| `ft_lstclear` | Empty list, head set to NULL after clearing. |
| `ft_lstiter` | Empty list, function application to each node. |
| `ft_lstmap` | Empty list, allocation failure handling during sequence. |

## 4. Extra - Additional Functions

Utilities not strictly required by the standard project but supported by this tester.

| Function | Edge Cases Tested |
| :--- | :--- |
| `ft_isblank` | Space and Horizontal Tab check. |
| `ft_iscntrl` | Control characters (0-31 and 127). |
| `ft_isgraph` | Printable characters excluding space. |
| `ft_islower` | 'a' through 'z' strictly. |
| `ft_isspace` | Spaces, tabs, newlines, vtabs, carriage returns. |
| `ft_isupper` | 'A' through 'Z' strictly. |
| `ft_isxdigit` | '0-9', 'a-f', 'A-F'. |
| `ft_itoa_base` | Bases 2-16, negative numbers, INT_MIN. |
| `ft_memccpy` | Character found/not found in `n` bytes. |
| `ft_str_is_alpha` | Check if string is only letters. |
| `ft_strcapitalize` | Capitalizing words after non-alphanumeric chars. |
| `ft_strcasecmp` | Case-insensitive comparison. |
| `ft_strndup` | `n` smaller/larger than `strlen`. |
| `ft_strtok` | Multiple delimiters, sequential calls. |
| `ft_strupcase` | Lowercase to uppercase transformation in-place. |
| `ft_strlowcase` | Uppercase to lowercase transformation in-place. |
| `ft_strcasestr` | Case-insensitive search of needle in haystack. |
