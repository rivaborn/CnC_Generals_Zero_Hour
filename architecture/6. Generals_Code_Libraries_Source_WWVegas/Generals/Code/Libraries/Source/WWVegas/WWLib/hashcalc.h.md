# Generals/Code/Libraries/Source/WWVegas/WWLib/hashcalc.h

## Purpose
Defines a template class for computing hash values for objects, supporting multiple hash values per object for floating-point comparisons.

## Responsibilities
- Provides abstract interface for hash calculation
- Supports epsilon-based matching for floating-point values
- Used by UniqueArrayClass and HashTableClass templates

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
- None

## Dependencies
- None (header-only, no external symbols)
