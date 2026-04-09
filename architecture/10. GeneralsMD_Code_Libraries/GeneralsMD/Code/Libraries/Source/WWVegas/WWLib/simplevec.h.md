# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/simplevec.h

## Purpose
Provides lightweight dynamic array templates for memory-copyable data types.

## Responsibilities
- Implements `SimpleVecClass` for fixed-size arrays
- Implements `SimpleDynVecClass` for dynamic arrays with automatic resizing
- Supports basic operations like add/delete/resize
- Uses `memcpy`/`memmove` for element manipulation

## Key Types
- **SimpleVecClass (Class)**: Fixed-size array wrapper for memory-copyable types
- **SimpleDynVecClass (Class)**: Dynamic array with automatic resizing (inherits from `SimpleVecClass`)

## Key Functions
### SimpleVecClass::Resize
- Purpose: Resizes the underlying array
- Calls: `W3DNEWARRAY`, `memcpy`, `delete[]`

### SimpleDynVecClass::Add
- Purpose: Adds an element to the end, growing if needed
- Calls: `Grow`

### SimpleDynVecClass::Delete
- Purpose: Removes an element by index
- Calls: `memmove`, `Shrink`

### SimpleDynVecClass::Grow
- Purpose: Expands the array by 25% or to a hint size
- Calls: `Resize`

### SimpleDynVecClass::Shrink
- Purpose: Reduces array size if usage is below 25%
- Calls: `Resize`

## Globals
- None

## Dependencies
- `always.h`, `assert.h`, `string.h`
- `W3DNEWARRAY` macro
- `MAX` macro
