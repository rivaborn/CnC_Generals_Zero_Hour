# Generals/Code/Libraries/Source/WWVegas/WWLib/MPMATH.H

## Purpose
Provides multi-precision arithmetic functions for cryptographic operations.

## Responsibilities
- Implements multi-precision integer arithmetic
- Supports modular arithmetic and primality testing
- Provides bit manipulation and encoding/decoding utilities
- Integrates with Straw RNG for random number generation

## Key Types
- `digit` (typedef unsigned long): Basic unit for multi-precision numbers
- `signeddigit` (typedef signed long): Signed version of digit

## Key Functions
### XMP_Add
- Purpose: Adds two multi-precision numbers
- Calls: None visible

### XMP_Mult
- Purpose: Multiplies two multi-precision numbers
- Calls: None visible

### XMP_Exponent_Mod
- Purpose: Computes modular exponentiation
- Calls: None visible

### XMP_Is_Prime
- Purpose: Primality test for multi-precision numbers
- Calls: XMP_Rabin_Miller_Test

## Globals
- `UNITSIZE` (const int): 32 (bit precision per digit)
- `MAX_BIT_PRECISION` (const int): 2048 (max bits for operations)

## Dependencies
- `bool.h`, `straw.h`, `<stdlib.h>`
- `Straw` class for random number generation
- External symbols: XMP_Fetch_Prime_Size, XMP_Fetch_Prime_Table
