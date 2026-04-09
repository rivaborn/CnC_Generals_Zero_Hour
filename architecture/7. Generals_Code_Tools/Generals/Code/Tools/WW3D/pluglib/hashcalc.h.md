# Generals/Code/Tools/WW3D/pluglib/hashcalc.h

## Purpose
Defines an abstract base class for computing hash values for objects, supporting multiple hash values per object.

## Responsibilities
- Declares pure virtual methods for hash computation and comparison
- Provides interface for hash table and unique array templates
- Supports epsilon-based floating-point comparisons

## Key Types
- HashCalculatorClass (Class): abstract base class for hash calculation logic

## Key Functions
### Items_Match
- Purpose: Compare two objects for equality (supports epsilon tests).
- Calls: None

### Compute_Hash
- Purpose: Compute hash value for a given object.
- Calls: None

### Num_Hash_Bits
- Purpose: Return number of bits needed for hash table allocation.
- Calls: None

### Num_Hash_Values
- Purpose: Return number of hash values per object.
- Calls: None

### Get_Hash_Value
- Purpose: Retrieve a specific hash value by index.
- Calls: None

## Globals
None

## Dependencies
- None (header-only, template class)
