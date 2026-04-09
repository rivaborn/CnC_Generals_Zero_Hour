# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/uarray.h

## Purpose
Implements a template class for storing unique objects using a hash table for efficient lookups.

## Responsibilities
- Maintains a dynamic array of unique items
- Uses a hash table to quickly detect duplicates
- Provides methods to add items and retrieve them by index
- Requires a HashCalculatorClass for the stored type

## Key Types
- **UniqueArrayClass<T> (Class)**: Template class for storing unique objects with hash-based duplicate detection.
- **HashItem (Class)**: Inner class holding an item and its next hash index.
- **(anonymous enum) (Enum)**: Defines NO_ITEM constant (0xFFFFFFFF).

## Key Functions
### UniqueArrayClass<T>::Add
- Purpose: Adds an item to the array if not already present, returns its index.
- Calls: HashCalculator->Compute_Hash, HashCalculator->Num_Hash_Values, HashCalculator->Get_Hash_Value, HashCalculator->Items_Match, UniqueItems.Add.

### UniqueArrayClass<T>::UniqueArrayClass
- Purpose: Constructor initializes hash table and vector.
- Calls: HashCalculator->Num_Hash_Bits, W3DNEWARRAY.

### UniqueArrayClass<T>::~UniqueArrayClass
- Purpose: Destructor cleans up hash table memory.
- Calls: delete[].

## Globals
- **NO_ITEM (int)**: Constant (0xFFFFFFFF) representing no item in hash table.

## Dependencies
- **hashcalc.h**: For HashCalculatorClass.
- **vector.h**: For DynamicVectorClass.
- **W3DNEWARRAY**: Memory allocation macro.
