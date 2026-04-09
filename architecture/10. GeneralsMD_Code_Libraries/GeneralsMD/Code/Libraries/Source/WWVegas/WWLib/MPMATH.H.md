# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/MPMATH.H

## Purpose
Header file for multi-precision arithmetic operations used in cryptographic functions.

## Responsibilities
- Defines constants and types for multi-precision math
- Declares functions for arithmetic operations (add, subtract, multiply, divide)
- Provides bit manipulation and encoding/decoding functions
- Supports modular arithmetic and primality testing

## Key Types
- `digit` (typedef unsigned long): Basic unit for multi-precision numbers
- `signeddigit` (typedef signed long): Signed version of digit

## Key Functions
### XMP_Add
- Purpose: Adds two multi-precision numbers with carry
- Calls: None visible

### XMP_Mult
- Purpose: Multiplies two multi-precision numbers
- Calls: None visible

### XMP_Mod_Mult
- Purpose: Performs modular multiplication
- Calls: None visible

### XMP_Is_Prime
- Purpose: Tests if a number is prime
- Calls: XMP_Rabin_Miller_Test, XMP_Fermat_Test

## Globals
- `UNITSIZE` (const int): Size of a digit in bits (32)
- `MAX_BIT_PRECISION` (const int): Maximum bit precision (2048)

## Dependencies
- "bool.h", "straw.h", <stdlib.h>
- Uses `Straw` class for random number generation
- External symbols: XMP_Fetch_Prime_Size, XMP_Fetch_Prime_Table
