# Generals/Code/Libraries/Source/WWVegas/WWLib/int.cpp

## Purpose
Implements basic big integer operations and prime number generation for cryptographic or mathematical use.

## Responsibilities
- Manages big integer arithmetic state (carry/borrow/error flags)
- Provides prime number generation
- Handles big integer remainder storage

## Key Types
- `bignum` (Class): wrapper for large integer operations with error tracking
- `BigInt` (Type): alias for `bignum` (not inferable)

## Key Functions
### `Generate_Prime`
- Purpose: Generates a prime number of specified bit length using a random number generator
- Calls: None (declaration only)

## Globals
- `bignum::Error` (int): tracks arithmetic error state
- `bignum::Carry` (bool): tracks carry flag state
- `bignum::Borrow` (bool): tracks borrow flag state
- `bignum::Remainder` (bignum): stores remainder from division operations

## Dependencies
- `always.h`, `int.h`, `mpmath.h`, `rng.h`
- `RandomNumberGenerator` (external class)
- `_MSC_VER` (compiler macro)
