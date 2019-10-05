# C++ Coding Style Standard

__The following outlines the coding style used in this project. 
Commits that break too many of these might get rejected.__

## The short version

Make it readable and understandable. Use the `.clang-format` supplied in this repo.

## The long version

* Names should *rarely* be or contain abbreviations.

* Names need to describe what something is doing, what its purpose is, etc. Names like `num1`, `var2`, `a`, `b`, `c`, `n`, etc are not acceptable. Good names are `normalized_velocity`, `length`, `load_config_file`. 
* Classes should be `CamelCase`.
* Functions, methods, variables, etc. should be `snake_case`.
* Enum items should be `CamelCase`.
* Getters should **not** start with `get`. Instead, they should have the name of the member they give access to, without the `m_` prefix. Example:  `m_velocity`'s getter would be `velocity()`.
* Member variables should start with `m_`.
* Setters should start with `set_`.
* Globals should start with `g_`.
* *No* type prefixes should be used, e.g. `f_` for float.
* Infinite loops should only be `for (;;)`.
* Template typename names should be `CamelCase`, prefixed by `_`. Examples: `_T`, `_Key`.
* Curly brackets should not be in the same line with other text (allowed exclusions are short single-liners in header files: constructors/destructors and get/set-like functions). 
* One statement per code line. `float x, y;` and similar is **not** allowed.
* No space between function’s name and parentheses "(".
* No space before comma, semicolon, and parentheses.
* Single space character after a comma.
* Single space character before and after binary arithmetic operators (+, -, *, /, *, /, %, &, &&, |, ||, |=, ==, +=, etc.) and before unary operators (-, !, ~, etc.).
* Single space character before and after '?' and ':' in the conditional/ternary operator.
* No spaces around < and > in template argument lists.
* Single space character between statement (if, while, for, switch, etc.) and the opening '('.
* No space after `template` keyword.
* Short blocks and functions on a single line are allowed.
* Indent is 4 spaces, no tabs.
* Access modifiers (`public`, `private`, etc) have same indent as their containing `class` or `struct` keyword.
* Spaces in and before C++11 initializer lists are required.
* Lines should not be longer than `90`.
* Case labels are indented by `4` spaces from their containing `switch` statements.

### A few more rules that are easier to show than to explain

Placement of `&`, `*`, `const`, etc.
    
**Correct:**
```cpp
int* ptrA = &var;
const int* ptrB = &var;
const int* const ptrC = &var;
int& refA = var;
const int& refB = var;
```
**Wrong:**
```cpp
int *ptrD = &var; // * on wrong side of the space
int const *ptrE = &var; // const on the wrong side
int &refC = var; // & on wrong side of the space
int const& refD = var; // const on the wrong side
```
... and so on.

<sub>Yes, this is taken mostly from CryEngine's C++ Coding Standard</sub>
