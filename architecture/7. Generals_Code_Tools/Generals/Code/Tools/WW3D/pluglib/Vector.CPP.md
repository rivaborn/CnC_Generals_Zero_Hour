# Generals/Code/Tools/WW3D/pluglib/Vector.CPP

## Purpose
Implements a bit-packed boolean vector class and a generic vector template class for dynamic array management.

## Responsibilities
- Manages bit-packed boolean arrays via `BooleanVectorClass`
- Provides dynamic resizing and memory management
- Supports copy construction and assignment
- Implements bit-level manipulation for boolean storage
- Handles generic vector operations via `VectorClass<T>`

## Key Types
- `BooleanVectorClass`: Bit-packed boolean array with dynamic resizing
- `VectorClass<T>`: Generic dynamic array template class

## Key Functions
### `BooleanVectorClass::Fixup`
- Purpose: Synchronizes the cached boolean value with the bit array
- Calls: `Set_Bit`, `Get_Bit`

### `BooleanVectorClass::Resize`
- Purpose: Resizes the bit-packed boolean array
- Calls: `BitArray.Resize`, `operator[]`

### `BooleanVectorClass::operator=`
- Purpose: Assigns one boolean vector to another
- Calls: `Fixup`

### `VectorClass<T>::Resize`
- Purpose: Resizes the generic vector
- Calls: Not inferable (template implementation)

## Globals
- None

## Dependencies
- `always.h`, `vector.h`, `string.h`
- `Set_Bit`, `Get_Bit` (bit manipulation functions)
- `memset` (from `string.h`)
