# Generals/Code/Libraries/Source/WWVegas/WWLib/simplevec.h

## Purpose
Provides lightweight dynamic array templates for simple, memcopy-able data types.

## Responsibilities
- Implements `SimpleVecClass` for fixed-size arrays
- Implements `SimpleDynVecClass` for dynamic arrays with automatic resizing
- Supports basic operations like add, delete, and resize
- Uses `memcpy`/`memmove` for element manipulation

## Key Types
- **SimpleVecClass (Class)**: Fixed-size array wrapper for memcopy-able types
- **SimpleDynVecClass (Class)**: Dynamic array with automatic resizing (inherits from `SimpleVecClass`)

## Key Functions
### SimpleVecClass::Resize
- Purpose: Resizes the underlying array, copying existing elements
- Calls: `W3DNEWARRAY`, `memcpy`, `delete[]`

### SimpleDynVecClass::Add
- Purpose: Adds an element to the end, growing the array if needed
- Calls: `Grow`

### SimpleDynVecClass::Delete
- Purpose: Removes an element by index, shifting remaining elements
- Calls: `memmove`, `Shrink`

### SimpleDynVecClass::Grow
- Purpose: Expands the array by 25% (or more if hinted)
- Calls: `Resize`

### SimpleDynVecClass::Shrink
- Purpose: Reduces array size if usage is below 25%
- Calls: `Resize`

## Globals
- None

## Dependencies
- `always.h`, `<assert.h>`, `<string.h>`
- `W3DNEWARRAY` (macro)
- `MAX` (macro)
