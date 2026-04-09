# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/smartptr.h

## Purpose
Template class for smart pointer management, providing basic reference semantics and safety checks.

## Responsibilities
- Wraps raw pointers with reference counting (implied)
- Provides operator overloads for pointer-like syntax
- Supports copy construction and assignment
- Includes validity checking via `Is_Valid()`

## Key Types
- **SmartPtr (Class)**: Template class managing a pointer with basic smart pointer functionality

## Key Functions
### SmartPtr (Constructor)
- Purpose: Initializes smart pointer from raw pointer or NoInitClass
- Calls: None

### operator= (Assignment)
- Purpose: Assigns another SmartPtr's pointer to this one
- Calls: None

### Is_Valid
- Purpose: Checks if the managed pointer is non-null
- Calls: None

### operator-> and operator*
- Purpose: Provides pointer-like access to the managed object
- Calls: None

## Globals
- None

## Dependencies
- `noinit.h` (included)
- `assert` (used in commented-out increment operators)
