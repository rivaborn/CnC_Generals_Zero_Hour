# Generals/Code/Libraries/Source/WWVegas/WWLib/ref_ptr.h

## Purpose
Implements a reference-counted smart pointer template class (`RefCountPtr`) for managing object lifetimes in the SAGE engine.

## Responsibilities
- Manages reference counts for objects implementing `Add_Ref()`/`Release_Ref()`.
- Provides safe pointer operations (dereferencing, assignment, comparison).
- Supports implicit null checks via `DummyPtrType` conversion.
- Handles type-safe conversions between related reference-counted types.

## Key Types
- **DummyPtrType (Class)**: Dummy type for null comparisons.
- **RefCountPtr<T> (Class)**: Smart pointer wrapper for reference-counted objects.
- **ReferenceHandling (Enum)**: Flags for `GET`/`PEEK` reference handling modes.

## Key Functions
### `operator==` (template)
- Purpose: Compares two `RefCountPtr` instances for equality.
- Calls: `Peek()` on both operands.

### `operator<` (template)
- Purpose: Orders two `RefCountPtr` instances.
- Calls: `Peek()` on both operands.

### `operator==` (DummyPtrType)
- Purpose: Enables `0 == ptr` comparisons.
- Calls: `Peek()` on the `RefCountPtr`.

### `operator!=` (DummyPtrType)
- Purpose: Enables `0 != ptr` comparisons.
- Calls: `Peek()` on the `RefCountPtr`.

## Globals
- **None**

## Dependencies
- `always.h` (for assertions)
- Requires objects to implement `Add_Ref()`/`Release_Ref()`.
