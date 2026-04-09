# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/fixed.cpp

## Purpose
Implements a fixed-point number class for the game engine, providing arithmetic and conversion utilities.

## Responsibilities
- Fixed-point number representation and arithmetic
- Conversion between fixed-point and ASCII strings
- Handling of fractional and percentage values

## Key Types
- `fixed` (Class): Fixed-point number with 8-bit whole and fractional parts
- `fixed::Data` (Union): Raw storage for fixed-point value (16-bit)
- `fixed::Composite` (Struct): Whole (8-bit) and Fraction (8-bit) components

## Key Functions
### `fixed::fixed(int numerator, int denominator)`
- Purpose: Constructs a fixed-point number from a fraction.
- Calls: None

### `fixed::fixed(char const * ascii)`
- Purpose: Parses an ASCII string into a fixed-point number (supports decimals and percentages).
- Calls: `atoi`, `strchr`, `isspace`, `isdigit`

### `fixed::To_ASCII(char * buffer, int maxlen)`
- Purpose: Converts the fixed-point number to an ASCII string.
- Calls: `sprintf`, `strlen`, `strncpy`

### `fixed::As_ASCII()`
- Purpose: Returns a static ASCII representation of the number.
- Calls: `To_ASCII`

## Globals
- `fixed::_1_2`, `_1_3`, `_1_4`, `_3_4`, `_2_3` (const fixed): Predefined fractional constants

## Dependencies
- `fixed.h` (header)
- `<string.h>`, `<stdlib.h>`, `<stdio.h>`, `<ctype.h>` (standard libraries)
