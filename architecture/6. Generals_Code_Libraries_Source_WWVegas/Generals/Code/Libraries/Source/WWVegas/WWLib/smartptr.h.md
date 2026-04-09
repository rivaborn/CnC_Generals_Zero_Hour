# Generals/Code/Libraries/Source/WWVegas/WWLib/smartptr.h

## Purpose
Provides a smart pointer template class for managing object lifetimes.

## Responsibilities
- Wraps raw pointers with basic reference semantics
- Supports pointer arithmetic (commented out)
- Provides null checks via `Is_Valid()`
- Enables pointer-like syntax (`->`, `*`, `=`)

## Key Types
- **SmartPtr (Class)**: A template class wrapping a raw pointer with basic smart pointer functionality.

## Key Functions
### SmartPtr (Constructor)
- Purpose: Initializes the smart pointer with a raw pointer or NoInitClass.
- Calls: None.

### ~SmartPtr (Destructor)
- Purpose: Nulls the internal pointer on destruction.
- Calls: None.

### Is_Valid
- Purpose: Checks if the internal pointer is non-null.
- Calls: None.

### operator=
- Purpose: Assigns another SmartPtr's pointer to this one.
- Calls: None.

### operator->
- Purpose: Dereferences the pointer for member access.
- Calls: None.

### operator*
- Purpose: Dereferences the pointer for value access.
- Calls: None.

## Globals
- None.

## Dependencies
- `noinit.h` (included)
- `assert` (used in commented-out pointer arithmetic)
