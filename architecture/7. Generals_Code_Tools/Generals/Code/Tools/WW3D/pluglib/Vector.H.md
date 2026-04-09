# Generals/Code/Tools/WW3D/pluglib/Vector.H

## Purpose
Generic vector container class template for dynamic array management.

## Responsibilities
- Provides resizable array storage for arbitrary types
- Supports dynamic addition/removal of elements
- Handles memory allocation/deallocation
- Offers pointer-to-index conversion and value-based lookup

## Key Types
- `VectorClass<T>` (class): Base template for fixed-size vector storage
- `DynamicVectorClass<T>` (class): Extends VectorClass with dynamic resizing
- `BooleanVectorClass` (class): Bit-packed boolean vector for memory efficiency

## Key Functions
### `VectorClass<T>::Resize`
- Purpose: Changes the vector size and optionally initializes from an array
- Calls: `new[]`, `delete[]`

### `DynamicVectorClass<T>::Add`
- Purpose: Appends an element, auto-resizing if needed
- Calls: `Resize`, `operator[]`

### `DynamicVectorClass<T>::Delete`
- Purpose: Removes element by index or value, shifting remaining elements
- Calls: `memmove`

### `BooleanVectorClass::operator[]`
- Purpose: Provides indexed access to bit-packed boolean values
- Calls: `Fixup`, `Get_Bit`

## Globals
- `Set_Bit`, `Get_Bit`, `First_True_Bit`, `First_False_Bit` (functions): Bit manipulation utilities

## Dependencies
- `<assert.h>`, `<new.h>`, `<string.h>`, `<stddef.h>`, `<stdlib.h>`
- `NoInitClass` (from "noinit.h")
- Memory allocation operators (`new`, `delete`)
