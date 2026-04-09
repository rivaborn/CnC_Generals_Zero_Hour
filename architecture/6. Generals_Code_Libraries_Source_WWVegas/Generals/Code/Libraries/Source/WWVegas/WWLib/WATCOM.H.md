# Generals/Code/Libraries/Source/WWVegas/WWLib/WATCOM.H

## Purpose
Header file for Watcom C++ compiler-specific configurations and macros.

## Responsibilities
- Defines Watcom-specific compiler directives and warnings
- Provides math constants not available in Borland C++
- Includes bool type definition

## Key Types
- None

## Key Functions
- None

## Globals
- M_E, M_LOG2E, M_LOG10E, M_LN2, M_LN10, M_PI, M_PI_2, M_PI_4, M_1_PI, M_2_PI, M_1_SQRTPI, M_2_SQRTPI, M_SQRT2, M_SQRT_2 (double): Math constants

## Dependencies
- "bool.h" (included)
- __WATCOMC__ (compiler macro)
- _MSC_VER (compiler macro)
