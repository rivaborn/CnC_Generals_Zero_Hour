# Generals/Code/Libraries/Source/WWVegas/WWLib/uarray.h

## Purpose
Implements a template class for storing unique objects using a hash table for efficient duplicate detection.

## Responsibilities
- Maintains a dynamic array of unique items
- Uses hash-based lookup to prevent duplicates
- Provides methods to add items and retrieve them by index
- Manages memory for the hash table

## Key Types
- **UniqueArrayClass<T> (Class)**: Template class for storing unique objects with hash-based duplicate detection.
- **HashItem (Class)**: Inner class representing an item in the unique array with a next hash index.
- **(anonymous enum) (Enum)**: Defines `NO_ITEM` constant for hash table initialization.

## Key Functions
### UniqueArrayClass<T>::Add
- Purpose: Adds an item to the array if it's not already present, returns its index.
- Calls: `HashCalculator->Compute_Hash`, `HashCalculator->Num_Hash_Values`, `HashCalculator->Get_Hash_Value`, `HashCalculator->Items_Match`, `UniqueItems.Add`

### UniqueArrayClass<T>::UniqueArrayClass
- Purpose: Constructor initializes the hash table and unique items vector.
- Calls: `HashCalculator->Num_Hash_Bits`, `W3DNEWARRAY`

### UniqueArrayClass<T>::~UniqueArrayClass
- Purpose: Destructor cleans up the hash table memory.
- Calls: `delete[]`

## Globals
- **NO_ITEM (int)**: Constant used to mark empty hash table entries.

## Dependencies
- `hashcalc.h` (HashCalculatorClass)
- `vector.h` (DynamicVectorClass)
- `W3DNEWARRAY` (memory allocation)
