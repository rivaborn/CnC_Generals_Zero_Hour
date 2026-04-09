# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/fixed.h

## Purpose
Defines a fixed-point number class for efficient fractional arithmetic without floating-point operations.

## Responsibilities
- Provides fixed-point arithmetic operations (add, subtract, multiply, divide)
- Supports bit-shift operations for performance
- Implements comparison operators for fixed-point and integer types
- Offers rounding, saturation, and inversion utilities
- Converts between fixed-point and ASCII/unsigned integer representations

## Key Types
- **fixed (Class)**: Fixed-point number with 8-bit whole and fractional parts (0-255.996)
- **(anonymous union)**: Internal storage (either raw 16-bit or split whole/fraction)
- **(anonymous struct)**: Whole/fraction byte layout (endianness-dependent)

## Key Functions
### fixed(int numerator, int denominator)
- Purpose: Constructs fixed-point from fraction
- Calls: None

### operator*(fixed const & rvalue)
- Purpose: Multiplies two fixed-point values
- Calls: None

### operator/(fixed const & rvalue)
- Purpose: Divides fixed-point by another fixed-point
- Calls: None

### Round_Up()
- Purpose: Rounds fixed-point value up
- Calls: None

### To_ASCII(char * buffer, int maxlen)
- Purpose: Converts fixed-point to string
- Calls: None

## Globals
- **_1_2 (fixed)**: Predefined constant (0.5)
- **_1_3 (fixed)**: Predefined constant (~0.333)
- **_1_4 (fixed)**: Predefined constant (0.25)
- **_3_4 (fixed)**: Predefined constant (0.75)
- **_2_3 (fixed)**: Predefined constant (~0.666)

## Dependencies
- **bool.h**: For boolean type
- **None**: No external symbols used
