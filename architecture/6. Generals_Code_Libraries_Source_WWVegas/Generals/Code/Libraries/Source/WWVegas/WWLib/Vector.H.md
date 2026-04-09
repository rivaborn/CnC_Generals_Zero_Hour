# Generals/Code/Libraries/Source/WWVegas/WWLib/Vector.H

## Purpose
This file defines template-based vector classes for dynamic array management in the SAGE engine.

## Responsibilities
- Provides `VectorClass<T>` for fixed-size arrays
- Implements `DynamicVectorClass<T>` for resizable arrays
- Includes `BooleanVectorClass` for space-efficient boolean storage
- Supports pointer-based and value-based indexing

## Key Types
- `VectorClass<T>` (class): Fixed-size dynamic array container
- `DynamicVectorClass<T>` (class): Resizable array container with growth management
- `BooleanVectorClass` (class): Bit-packed boolean array
- `NoInitClass` (class): Marker for uninitialized vector construction

## Key Functions
### `VectorClass<T>::Resize`
- Purpose: Changes the size of the vector
- Calls: `W3DNEWARRAY`, `delete[]`

### `DynamicVectorClass<T>::Add`
- Purpose: Appends an element to the dynamic vector
- Calls: `Resize`, `memmove`

### `BooleanVectorClass::operator[]`
- Purpose: Provides indexed access to bit-packed booleans
- Calls: `Fixup`, `Get_Bit`

## Globals
- `W3DNEWARRAY`: Memory allocation macro
- `Set_Bit`, `Get_Bit`, `First_True_Bit`, `First_False_Bit`: Bit manipulation functions

## Dependencies
- `always.h`, `assert.h`, `stdlib.h`, `string.h`
- `W3DNEWARRAY` macro
- `memmove` function
