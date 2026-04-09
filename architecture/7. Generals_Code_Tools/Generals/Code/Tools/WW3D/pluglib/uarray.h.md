# Generals/Code/Tools/WW3D/pluglib/uarray.h

## Purpose
Template class for managing arrays of unique objects using hashing for efficient duplicate detection.

## Responsibilities
- Maintain a dynamic array of unique items
- Use hash table for fast duplicate detection
- Provide methods to add items and access them by index
- Require a HashCalculatorClass for the stored type

## Key Types
- **UniqueArrayClass<T> (Class)**: Main container for unique items with hash-based lookup
- **HashItem (Class)**: Internal structure holding an item and its next hash index
- **(anonymous enum) (Enum)**: Defines NO_ITEM constant (0xFFFFFFFF)

## Key Functions
### UniqueArrayClass<T>::Add
- Purpose: Adds a new item if not already present, returns its index
- Calls: HashCalculator->Compute_Hash, HashCalculator->Num_Hash_Values, HashCalculator->Get_Hash_Value, HashCalculator->Items_Match, UniqueItems.Add

### UniqueArrayClass<T>::UniqueArrayClass
- Purpose: Constructor initializing hash table and growth parameters
- Calls: None directly (initializes members)

### UniqueArrayClass<T>::~UniqueArrayClass
- Purpose: Destructor cleaning up hash table memory
- Calls: delete[] on HashTable

## Globals
- **NO_ITEM (const)**: Hash table sentinel value (0xFFFFFFFF)

## Dependencies
- "hashcalc.h" (HashCalculatorClass)
- "vector.h" (DynamicVectorClass)
- Uses templates and standard C++ memory management
