# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/INT.H

## Purpose
Defines a templated arbitrary-precision integer class (`Int`) and related utilities for cryptographic and mathematical operations.

## Responsibilities
- Provides arbitrary-precision integer arithmetic (addition, subtraction, multiplication, division).
- Supports bitwise operations, comparisons, and number-theoretic functions (GCD, primality testing).
- Handles encoding/decoding of integers in various formats (ASCII, DER).
- Implements modular exponentiation and inverse operations for cryptography.

## Key Types
- `Int<PRECISION>` (Class): Arbitrary-precision integer with configurable precision.
- `RemainderTable<T>` (Struct): Precomputes remainders for modular arithmetic optimization.
- `bignum` (Typedef): Alias for `Int<MAX_UNIT_PRECISION>`.
- `BigInt` (Typedef): Alias for `Int<MAX_UNIT_PRECISION>`.

## Key Functions
### `Int::exp_b_mod_c`
- Purpose: Computes modular exponentiation (b^e mod m).
- Calls: `XMP_Exponent_Mod`

### `Int::Gcd`
- Purpose: Computes greatest common divisor of two integers.
- Calls: None (implemented directly).

### `Generate_Prime`
- Purpose: Generates a prime number of specified bit length.
- Calls: `Int::Randomize`, `Int::IsPrime`, `RemainderTable::Increment`

## Globals
- `Int::Error` (int): Stores error state from last operation.
- `Int::Carry` (bool): Carry flag from last addition.
- `Int::Borrow` (bool): Borrow flag from last subtraction.
- `Int::Remainder` (Int): Remainder from last division.

## Dependencies
- `mpmath.h`: External multiprecision math functions (e.g., `XMP_Add`, `XMP_Signed_Mult`).
- `straw.h`: Random number generation (`Straw` class).
- `<assert.h>`, `<limits.h>`, `<memory.h>`: Standard C headers.
