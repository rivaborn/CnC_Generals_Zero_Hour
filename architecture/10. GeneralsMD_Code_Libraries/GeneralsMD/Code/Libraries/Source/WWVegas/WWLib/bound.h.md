# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bound.h

## Purpose
Provides a templated function to clamp a value within a specified range.

## Responsibilities
- Defines a generic `Bound` function template
- Ensures values stay within min/max limits
- Supports multiple data types via templates
- Includes platform-specific conditional compilation

## Key Types
None

## Key Functions
### Bound
- Purpose: Clamps a value between a minimum and maximum.
- Calls: None

## Globals
None

## Dependencies
- Platform-specific preprocessor directives (`_MSC_VER`, `__WATCOMC__`)
- Standard C++ template mechanism
