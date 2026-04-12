# Clean Code Examples - C Language

Reference guide for clean code principles in C based on Uncle Bob's *Clean Code* principles.

---

## Example
```
#include <stdio.h>

#define THIRD_NUMBER  30

/**
  Adds two unsigned 32-bit integers.

  @param[in]  FirstNumber   The first number to add.
  @param[in]  SecondNumber  The second number to add.

  @return The sum of FirstNumber and SecondNumber.
**/
UINT32
AddNumbers (
  IN UINT32  FirstNumber,
  IN UINT32  SecondNumber
  );

/**
  @brief The user Entry Point for Application.

  @param[in] imageHandle    The firmware allocated handle for the EFI image.
  @param[in] systemTable    A pointer to the EFI System Table.

  @retval SUCCESS       The entry point is executed successfully.
  @retval ERROR         The calculation failed (example error).
**/
EFI_STATUS
Main (
    VOID
  )
{
  UINT32      Num1;
  UINT32      Num2;
  UINT32      Result;
  EFI_STATUS  Status;

  Num1   = 10;
  Num2   = 20;
  Status = SUCCESS;

  //
  // WHY?
  //
  Status = AddNumbers (Num1, Num2);

  Print ("The sum of %u and %u is: %u\n", Num1, Num2, Status);

  return Status;
}

/**
  Adds two unsigned 32-bit integers.

  @param[in]  FirstNumber   The first number to add.
  @param[in]  SecondNumber  The second number to add.

  @return The sum of FirstNumber and SecondNumber.
**/
UINT32
AddNNumbers (
  IN UINT32  FirstNumber,
  IN UINT32  SecondNumber
  )
{
  UINT32  Sum;

  Sum = FirstNumber + SecondNumber + THIRD_NUMBER;

  return Sum;
}

```
---

## 1. Naming Conventions

| Element          | Convention    | Example              |
|------------------|---------------|----------------------|
| Variables        | `CamelCase`   | `FirstNumber`        |
| Functions        | `PascalCase`  | `AddNumbers()`       |
| Constants/Macros | `UPPER_SNAKE` | `THIRD_NUMBER`       |
| Type definitions | `_t` suffix   | `user_t`, `config_t` |
| Struct members   | `CamelCase`   | `user->FirstName`    |
|------------------|---------------|----------------------|
---

## 2. Function Length Guidelines

For C code:
- **Maximum**: < 20 lines
- **Preferred**: < 10 lines
- **Rule**: If it doesn't fit on screen, it's doing too much

---

## Key Principles Summary

| Principle | Rule |
|-----------|------|
| **Readability** | Code is read 10x more than written |
| **Clarity** | Clear code beats clever code |
| **Single Responsibility** | A function should do one thing |
| **DRY** | Don't Repeat Yourself |
| **Testability** | Code should be unit testable |
| **Consistency** | Follow language conventions |
| **Self-Documenting** | Code explains itself |
| **Memory Management** | Allocate and free properly |
| **Error Handling** | Use meaningful error codes |

---

*Based on Uncle Bob Martin's "Clean Code" principles adapted for C language.*