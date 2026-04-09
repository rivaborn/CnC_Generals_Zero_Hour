# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/gcd_lcm.cpp

## Purpose
Implements mathematical functions for computing greatest common divisor (GCD) and least common multiple (LCM).

## Responsibilities
- Provides GCD calculation using Euclid's algorithm
- Provides LCM calculation based on GCD
- Handles unsigned integer inputs

## Key Types
None

## Key Functions
### Greatest_Common_Divisor
- Purpose: Computes the greatest common divisor of two unsigned integers using Euclid's algorithm
- Calls: Greatest_Common_Divisor (recursive)

### Least_Common_Multiple
- Purpose: Computes the least common multiple of two unsigned integers
- Calls: Greatest_Common_Divisor

## Globals
None

## Dependencies
- Key includes: "gcd_lcm.h"
