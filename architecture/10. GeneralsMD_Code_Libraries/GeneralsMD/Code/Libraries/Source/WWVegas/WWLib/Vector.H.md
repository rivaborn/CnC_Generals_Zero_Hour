# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Vector.H

## Purpose
Generic vector container class implementation for the SAGE engine, supporting dynamic resizing and element management.

## Responsibilities
- Provides templated vector container with dynamic resizing
- Supports both fixed and dynamic vector variants
- Implements element addition/removal and memory management
- Includes specialized boolean vector for bit-packed storage
- Offers pointer-based and value-based element identification

## Key Types
- `VectorClass<T>` (class): Base templated vector container
- `DynamicVectorClass<T>` (class): Extends VectorClass with dynamic growth
- `BooleanVectorClass` (class): Bit-packed boolean vector
- `NoInitClass` (class): Marker for uninitialized vector construction

## Key Functions
### `VectorClass<T>::Resize`
- Purpose: Changes vector size and optionally copies data
- Calls: `W3DNEWARRAY`, `Clear`

### `DynamicVectorClass<T>::Add`
- Purpose: Appends element to dynamic vector with growth handling
- Calls: `Resize`, `memmove`

### `DynamicVectorClass<T>::Delete`
- Purpose: Removes element by value or index with gap filling
- Calls: `ID`, `memmove`

### `BooleanVectorClass::operator[]`
- Purpose: Provides indexed access to bit-packed boolean values
- Calls: `Fixup`, `Get_Bit`

## Globals
- `W3DNEWARRAY` (macro): Memory allocation wrapper
- Bit manipulation functions (`Set_Bit`, `Get_Bit`, etc.)

## Dependencies
- `always.h`, `assert.h`, `stdlib.h`, `string.h`, `new.h`
- `W3DNEWARRAY` macro (memory allocation)
- Standard C++ template mechanisms
