# Generals/Code/Libraries/Source/WWVegas/WWLib/bool.h

## Purpose
Defines the `bool` type for C++ compatibility in older compilers.

## Responsibilities
- Provides a `bool` type definition for compilers lacking native support
- Ensures consistent boolean behavior across different platforms
- Includes conditional compilation for different compiler environments

## Key Types
- `bool` (Type): Boolean type definition for C++ compatibility

## Key Functions
None

## Globals
None

## Dependencies
- `yvals.h` (include): Used for MSVC-specific boolean handling
- `_MSC_VER`, `__BORLANDC__`, `__WATCOMC__` (preprocessor symbols): Compiler detection
- `TRUE_FALSE_DEFINED` (macro): Guard against multiple definitions
