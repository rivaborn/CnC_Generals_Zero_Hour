# Generals/Code/Libraries/Source/WWVegas/WWLib/vector.cpp

## Purpose
Implements a bit-packed boolean vector class and a generic vector class template for dynamic array management.

## Responsibilities
- Manages bit-packed boolean arrays via `BooleanVectorClass`
- Provides dynamic resizing and memory management
- Supports copy/assignment operations for both boolean and generic vectors
- Handles bit-level operations for boolean storage

## Key Types
- `BooleanVectorClass`: Bit-packed boolean array with dynamic resizing
- `VectorClass<T>`: Generic dynamic array template (declared in header)
- `BitArrayClass`: Underlying byte array for bit storage (external)

## Key Functions
### `BooleanVectorClass::Resize`
- Purpose: Resizes the boolean vector, clearing new bits if expanded
- Calls: `Fixup()`, `BitArray.Resize()`, `operator[]`

### `BooleanVectorClass::Fixup`
- Purpose: Synchronizes the internal copy buffer with the bit array
- Calls: `Set_Bit()`, `Get_Bit()` (external)

### `BooleanVectorClass::Reset`
- Purpose: Clears all boolean values to false
- Calls: `memset()`

### `BooleanVectorClass::Set`
- Purpose: Sets all boolean values to true
- Calls: `memset()`

## Globals
- None

## Dependencies
- `vector.h` (header with `VectorClass` template)
- `always.h` (assertions)
- `string.h` (`memset`)
- `Set_Bit()`, `Get_Bit()` (external bit manipulation functions)
