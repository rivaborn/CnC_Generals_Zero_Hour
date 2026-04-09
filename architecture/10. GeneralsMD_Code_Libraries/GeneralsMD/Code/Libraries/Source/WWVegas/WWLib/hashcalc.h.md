# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hashcalc.h

## Purpose
Defines an abstract base class for computing hash values for objects, supporting multiple hash values per object.

## Responsibilities
- Provides interface for hash calculation and comparison
- Supports floating-point epsilon-based matching
- Used by UniqueArrayClass and HashTableClass templates

## Key Types
- HashCalculatorClass (Class): abstract base class for hash calculation logic

## Key Functions
### Items_Match
- Purpose: Compare two objects for equality (with epsilon support).
- Calls: None

### Compute_Hash
- Purpose: Compute hash value for an object.
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
- None (header-only, template class)
