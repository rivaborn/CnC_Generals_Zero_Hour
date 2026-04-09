# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/noinit.h

## Purpose
Defines a placeholder class for zero-initialization of objects with virtual functions to enable safe serialization.

## Responsibilities
- Provides a no-op constructor wrapper for uninitialized object construction
- Enables direct memory loading into classes with virtual functions
- Facilitates in-place new operations after deserialization

## Key Types
- NoInitClass (Class): placeholder class for zero-initialization of objects with virtual functions

## Key Functions
### NoInitClass::operator()
- Purpose: no-op function called during construction to ensure virtual table pointer is set
- Calls: None

## Globals
- None

## Dependencies
- None
