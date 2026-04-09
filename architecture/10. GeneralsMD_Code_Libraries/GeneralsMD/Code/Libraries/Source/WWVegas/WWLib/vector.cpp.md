# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/vector.cpp

## Purpose
Implements a bit-packed boolean vector class and a generic vector class template for dynamic array management.

## Responsibilities
- Manages bit-packed boolean arrays via `BooleanVectorClass`
- Provides dynamic resizing and memory management
- Supports copy operations and comparisons for both boolean and generic vectors
- Handles bit-level operations for boolean storage

## Key Types
- `BooleanVectorClass`: Bit-packed boolean array with dynamic resizing
- `VectorClass<T>`: Generic dynamic array template class

## Key Functions
### `BooleanVectorClass::Resize`
- Purpose: Resizes the boolean vector, clearing new bits if expanded
- Calls: `Fixup()`, `BitArray.Resize()`

### `BooleanVectorClass::Fixup`
- Purpose: Synchronizes the internal copy buffer with the bit array
- Calls: `Set_Bit()`, `Get_Bit()`

### `BooleanVectorClass::operator=`
- Purpose: Assigns one boolean vector to another
- Calls: `Fixup()`

### `VectorClass<T>::Resize`
- Purpose: Resizes the generic vector
- Calls: `Clear()`

## Globals
- None

## Dependencies
- `vector.h` (header with class declarations)
- `always.h` (likely for macros/asserts)
- `string.h` (for `memset`)
- `Set_Bit()`, `Get_Bit()` (external bit manipulation functions)
