# Generals/Code/Libraries/Source/WWVegas/WWLib/visualc.h

## Purpose
Configures Microsoft Visual C++ compiler settings and defines mathematical constants for the game.

## Responsibilities
- Disables specific compiler warnings
- Sets inline depth for the compiler
- Defines mathematical constants (M_E, M_PI, etc.)
- Includes the bool.h header for bool type support

## Key Types
None

## Key Functions
None

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
- M_SQRT_2 (double): Square root of 2 (alternate form)

## Dependencies
- bool.h: For bool type definition
- _MSC_VER: Compiler version check
- pragma directives: For compiler configuration
