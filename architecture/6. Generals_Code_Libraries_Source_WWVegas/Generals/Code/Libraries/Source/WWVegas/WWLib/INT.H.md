# Generals/Code/Libraries/Source/WWVegas/WWLib/INT.H

## Purpose
Defines a templated arbitrary-precision integer class (`Int`) and related utilities for cryptographic and mathematical operations.

## Responsibilities
- Provides arbitrary-precision integer arithmetic (addition, subtraction, multiplication, division).
- Supports bitwise operations, comparisons, and number-theoretic functions (GCD, primality testing).
- Implements modular exponentiation and encoding/decoding for cryptographic use.
- Manages remainder tables for efficient modular arithmetic.
- Generates prime numbers for cryptographic applications.

## Key Types
- `Int<PRECISION>` (Class): Arbitrary-precision integer with configurable precision.
- `RemainderTable<T>` (Struct): Optimizes modular arithmetic by precomputing remainders.
- `bignum` (Typedef): Alias for `Int<MAX_UNIT_PRECISION>`.
- `BigInt` (Typedef): Alias for `Int<MAX_UNIT_PRECISION>`.

## Key Functions
### `Int::exp_b_mod_c`
- Purpose: Computes modular exponentiation (b^e mod m).
- Calls: `XMP_Exponent_Mod`

### `Int::Inverse`
- Purpose: Computes modular inverse (a^-1 mod m).
- Calls: `XMP_Inverse_A_Mod_B`

### `Generate_Prime`
- Purpose: Generates a prime number of specified bit length.
- Calls: `Randomize`, `IsPrime`, `RemainderTable` methods.

## Globals
- `Int::Error` (int): Tracks error state of last operation.
- `Int::Carry` (bool): Result of last addition.
- `Int::Borrow` (bool): Result of last subtraction.
- `Int::Remainder` (Int): Remainder from last division.

## Dependencies
- `mpmath.h`: Core multiprecision math functions (`XMP_*`).
- `straw.h`: Random number generation (`Straw`).
- `<assert.h>`, `<limits.h>`, `<memory.h>`: Standard C headers.
