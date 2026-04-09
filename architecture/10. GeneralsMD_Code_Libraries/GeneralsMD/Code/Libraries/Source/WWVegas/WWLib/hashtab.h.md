# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hashtab.h

## Purpose
Header file defining a template-based hash table class for managing named objects.

## Responsibilities
- Declares `NamedObjectHashTableClass` template for object storage/retrieval by key
- Defines hash table structure with chaining for collision resolution
- Provides interface for adding, removing, and finding objects

## Key Types
- `NamedObjectHashTableClass<Object,Key>` (Class): Hash table for named objects
- `HashItem` (Struct): Internal node linking object to next hash index
- `HashCalculatorClass<Key>` (Pointer): Abstract hasher for key types

## Key Functions
### `Add(Object * new_item, Key * key)`
- Purpose: Inserts an object into the hash table with a given key
- Calls: `HashCalculator->Compute_Hash`, `HashCalculator->Get_Hash_Value`

### `Remove(Object * item, Key * key)`
- Purpose: Removes an object from the hash table
- Calls: Not inferable

### `Find(const Key & key)`
- Purpose: Retrieves an object by its key
- Calls: `HashCalculator->Compute_Hash`, `HashCalculator->Get_Hash_Value`, `HashCalculator->Items_Match`

## Globals
- None

## Dependencies
- `DynamicVectorClass` for internal storage
- `HashCalculatorClass` for key hashing
- Standard C++ template mechanisms
