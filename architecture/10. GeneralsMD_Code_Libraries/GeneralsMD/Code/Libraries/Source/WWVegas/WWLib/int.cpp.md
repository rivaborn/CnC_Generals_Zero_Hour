# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/int.cpp

## Purpose
Implements basic big integer operations and prime number generation for cryptographic or mathematical use.

## Responsibilities
- Manages big integer arithmetic state (carry/borrow/error flags)
- Provides prime number generation
- Handles remainder storage during division
- Supports modular arithmetic

## Key Types
- bignum (Class): wrapper for arbitrary-precision integer operations
- BigInt (Type alias): likely typedef for bignum or similar

## Key Functions
### Generate_Prime
- Purpose: Generates a prime number of specified bit length
- Calls: None visible in this file

## Globals
- bignum::Error (int): tracks arithmetic error state
- bignum::Carry (bool): tracks carry flag state
- bignum::Borrow (bool): tracks borrow flag state
- bignum::Remainder (bignum): stores remainder from division operations

## Dependencies
- "always.h", "int.h", "mpmath.h", "rng.h"
- RandomNumberGenerator class
- BigInt type (likely defined elsewhere)
