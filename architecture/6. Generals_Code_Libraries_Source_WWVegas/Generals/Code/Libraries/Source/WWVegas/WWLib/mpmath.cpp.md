# Generals/Code/Libraries/Source/WWVegas/WWLib/mpmath.cpp

## Purpose
Implements multi-precision arithmetic operations for large integers, including encoding/decoding, arithmetic, bit manipulation, and primality testing.

## Responsibilities
- Multi-precision integer arithmetic (add, subtract, multiply, divide)
- Bit manipulation operations (shifts, rotations, NOT)
- Number theory operations (primality testing, modular exponentiation)
- Encoding/decoding of multi-precision numbers (DER, ASCII)
- Random number generation for cryptographic purposes

## Key Types
- `digit` (Type): Base unit for multi-precision numbers (unsigned short)
- `Straw` (Class): Random number generator interface
- `primeTable` (Array): Precomputed list of small prime numbers

## Key Functions
### XMP_Is_Prime
- Purpose: Determines if a multi-precision number is prime
- Calls: XMP_Is_Small_Prime, XMP_Small_Divisors_Test, XMP_Fermat_Test

### XMP_Exponent_Mod
- Purpose: Performs modular exponentiation (a^b mod c)
- Calls: XMP_Mod_Mult, XMP_Shift_Left_Bits, XMP_Shift_Right_Bits

### XMP_Mod_Mult
- Purpose: Performs multiplication followed by modulus operation
- Calls: XMP_Prepare_Modulus, XMP_Mod_Mult_Clear

### XMP_Rabin_Miller_Test
- Purpose: Performs Rabin-Miller primality test
- Calls: XMP_Exponent_Mod, XMP_Compare, XMP_Test_Eq_Int

### XMP_DER_Encode/Decode
- Purpose: Encodes/decodes numbers using Distinguished Encoding Rules
- Calls: XMP_Encode, XMP_DER_Length_Encode, XMP_Signed_Decode

## Globals
- `primeTable` (unsigned short[]): Precomputed list of primes < 32719
- `_modulus_shift` (int): Temporary storage for modulus operations
- `_modulus_bit_count` (int): Bit count for modulus operations

## Dependencies
- `mpmath.h`: Header for multi-precision math functions
- `always.h`: Common definitions
- `win.h`: Windows-specific types
- `Straw` class: Random number generator interface
