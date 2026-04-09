# Generals/Code/Libraries/Source/WWVegas/WWLib/noinit.h

## Purpose
Defines a placeholder class for zero-initialization of objects with virtual functions to enable safe serialization.

## Responsibilities
- Provides a no-op constructor parameter for zero-initialization
- Enables safe loading/saving of polymorphic objects via placement new
- Prevents unintended initialization of data members during construction

## Key Types
- NoInitClass (Class): placeholder class with no-op operator() for zero-initialization

## Key Functions
### NoInitClass::operator()
- Purpose: No-op function used as a constructor parameter for zero-initialization
- Calls: None

## Globals
- None

## Dependencies
- None
