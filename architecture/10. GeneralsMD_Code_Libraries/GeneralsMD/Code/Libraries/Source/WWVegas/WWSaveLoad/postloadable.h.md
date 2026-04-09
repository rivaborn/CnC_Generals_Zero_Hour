# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/postloadable.h

## Purpose
Defines a lightweight base class for objects that need post-load initialization without full PersistClass requirements.

## Responsibilities
- Provides a virtual `On_Post_Load` hook for derived classes.
- Manages post-load registration state via `IsPostLoadRegistered`.
- Simplifies integration with the SaveLoadSystem for non-Persist objects.

## Key Types
- **PostLoadableClass (Class)**: Base class for objects requiring post-load callbacks.

## Key Functions
### PostLoadableClass::On_Post_Load
- Purpose: Virtual hook called after object loading.
- Calls: None.

### PostLoadableClass::Is_Post_Load_Registered
- Purpose: Returns the registration state.
- Calls: None.

### PostLoadableClass::Set_Post_Load_Registered
- Purpose: Sets the registration state.
- Calls: None.

## Globals
- None.

## Dependencies
- No external includes or symbols. Standalone header.
