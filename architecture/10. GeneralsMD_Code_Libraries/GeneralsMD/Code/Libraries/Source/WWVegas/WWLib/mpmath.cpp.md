# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mpmath.cpp

## Purpose
Implements multi-precision arithmetic operations for large integers, including encoding/decoding, arithmetic, bit manipulation, and primality testing.

## Responsibilities
- Provides multi-precision integer arithmetic (add, subtract, multiply, divide)
- Implements bit manipulation operations (shifts, rotations, NOT)
- Handles encoding/decoding of multi-precision numbers (DER, ASCII)
- Performs primality testing (Fermat, Rabin-Miller)
- Manages modular arithmetic operations

## Key Types
- `digit` (Type): Base unit for multi-precision numbers (unsigned long)
- `Straw` (Class): Random number generator interface
- `primeTable` (Array): Precomputed list of small primes

## Key Functions
### `XMP_Add`
- Purpose: Adds two multi-precision numbers with optional carry
- Calls: None directly visible

### `XMP_Mult`
- Purpose: Multiplies two multi-precision numbers
- Calls: `XMP_Unsigned_Mult`, `XMP_Signed_Mult`

### `XMP_Is_Prime`
- Purpose: Tests if a multi-precision number is prime
- Calls: `XMP_Is_Small_Prime`, `XMP_Small_Divisors_Test`, `XMP_Fermat_Test`

### `XMP_Exponent_Mod`
- Purpose: Computes modular exponentiation
- Calls: `XMP_Mod_Mult`, `XMP_Shift_Right_Bits`

### `XMP_Rabin_Miller_Test`
- Purpose: Performs Rabin-Miller primality test
- Calls: `XMP_Exponent_Mod`, `XMP_Compare`

## Globals
- `primeTable` (unsigned short[]): Precomputed list of small primes
- `_modulus_shift` (int): Temporary storage for modulus operations
- `_modulus_bit_count` (int): Bit count for modulus operations

## Dependencies
- `mpmath.h`: Header for multi-precision math functions
- `always.h`: Common definitions
- `win.h`: Windows-specific types
- `Straw` class: Random number generation interface
