# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/WATCOM.H

## Purpose
Header file for Watcom C++ compiler-specific configurations and definitions.

## Responsibilities
- Configures Watcom compiler warnings and pragmas
- Defines mathematical constants for Watcom
- Includes bool.h for boolean type support

## Key Types
- None

## Key Functions
- None

## Globals
- M_E (double): Euler's number
- M_LOG2E (double): Log base 2 of E
- M_LOG10E (double): Log base 10 of E
- M_LN2 (double): Natural log of 2
- M_LN10 (double): Natural log of 10
- M_PI (double): Pi
- M_PI_2 (double): Pi/2
- M_PI_4 (double): Pi/4
- M_1_PI (double): 1/Pi
- M_2_PI (double): 2/Pi
- M_1_SQRTPI (double): 1/sqrt(Pi)
- M_2_SQRTPI (double): 2/sqrt(Pi)
- M_SQRT2 (double): Square root of 2
- M_SQRT_2 (double): Square root of 2 (alternate)

## Dependencies
- bool.h: For boolean type definition
- __WATCOMC__: Watcom compiler macro
- _MSC_VER: Microsoft compiler version macro
