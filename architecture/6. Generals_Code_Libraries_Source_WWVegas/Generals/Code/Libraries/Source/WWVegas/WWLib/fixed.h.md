# Generals/Code/Libraries/Source/WWVegas/WWLib/fixed.h

## Purpose
Defines a fixed-point number class for efficient fractional arithmetic without floating-point operations.

## Responsibilities
- Provides fixed-point arithmetic operations (add, subtract, multiply, divide)
- Supports bit-shift operations for performance
- Implements comparison operators for fixed-point and integer types
- Offers rounding, saturation, and inversion utilities
- Converts between fixed-point and ASCII/unsigned integer representations

## Key Types
- **fixed (Class)**: Fixed-point number with 8-bit whole and fractional parts
- **(anonymous union)**: Internal data storage (Composite or Raw)
- **(anonymous struct)**: Whole/Fraction byte layout

## Key Functions
### fixed(int numerator, int denominator)
- Purpose: Constructs fixed-point from numerator/denominator.
- Calls: None

### operator*(fixed const & rvalue)
- Purpose: Multiplies two fixed-point values.
- Calls: None

### Round_Up()
- Purpose: Rounds fixed-point value up.
- Calls: None

### To_ASCII(char * buffer, int maxlen)
- Purpose: Converts fixed-point to ASCII string.
- Calls: None

## Globals
- **_1_2, _1_3, _1_4, _3_4, _2_3 (fixed)**: Predefined fractional constants.

## Dependencies
- `bool.h` (for boolean type)
- Uses `unsigned char`, `unsigned short`, and `int` types.
