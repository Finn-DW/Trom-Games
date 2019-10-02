# C++ Coding Style Standard

__The following outlines the coding style used in this project. 
Commits that break too many of these might get rejected.__

## The short version

Make it readable and understandable.

## The long version

* Names should *rarely* be or contain abbreviations.

* Names need to describe what something is doing, what its purpose is, etc. Names like `num1`, `var2`, `a`, `b`, `c`, `n`, etc are not acceptable.

* Curly brackets should not be in the same line with other text (allowed exclusions are short single-liners in header files: constructors/destructors and get/set-like functions). Examples:
    
    Correct:
    ```cpp
    if (...)
    {
        ...
    }
    else
    {
        ...
    }
    ```
    Wrong:
    ```cpp
    if (...) {
        ...
    } else {
        ...
    }
    ```
* Opening and closing curly brackets should be on the same column.
* One statement per code line. `float x, y;` and similar is **not** allowed.
* No space between function’s name and parentheses "(".
* No space before comma, semicolon, and parentheses.
* Single space character after a comma.
* Single space character before and after binary arithmetic operators (+, -, *, /, *, /, %, &, &&, |, ||, |=, ==, +=, etc.) and before unary operators (-, !, ~, etc.).
* Single space character before and after '?' and ':' in the conditional/ternary operator.
* No spaces around < and > in template argument lists.
* Single space character between statement (if, while, for, switch, etc.) and the opening '('.

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
