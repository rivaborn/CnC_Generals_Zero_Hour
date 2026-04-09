# Generals/Code/Libraries/Source/WWVegas/WWLib/hashtab.h

## Purpose
Header file for a template-based hash table implementation in the Westwood Library.

## Responsibilities
- Defines `NamedObjectHashTableClass` template for key-value storage.
- Provides hash table operations (add, remove, find).
- Uses `HashCalculatorClass` for key hashing.

## Key Types
- `NamedObjectHashTableClass<Object,Key>` (Class): Generic hash table mapping keys to objects.
- `HashItem` (Struct): Internal node storing object pointer and next hash index.
- `HashCalculatorClass<Key>` (Class): External hasher for key computation.

## Key Functions
### `Add(Object * new_item, Key * key)`
- Purpose: Inserts an object into the hash table with a given key.
- Calls: `HashCalculator->Compute_Hash`, `HashCalculator->Get_Hash_Value`.

### `Remove(Object * item, Key * key)`
- Purpose: Removes an object from the hash table by key.
- Calls: Not inferable.

### `Find(const Key & key)`
- Purpose: Retrieves an object by its key.
- Calls: `HashCalculator->Compute_Hash`, `HashCalculator->Get_Hash_Value`, `HashCalculator->Items_Match`.

## Globals
- None

## Dependencies
- `DynamicVectorClass` (used for `Items` storage).
- `HashCalculatorClass` (external hashing interface).
