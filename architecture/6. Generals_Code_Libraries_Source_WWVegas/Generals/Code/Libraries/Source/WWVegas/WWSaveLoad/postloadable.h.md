# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/postloadable.h

## Purpose
Defines a lightweight base class for objects needing post-load callbacks without full PersistClass requirements.

## Responsibilities
- Provides virtual `On_Post_Load` hook for post-load processing
- Manages registration state via `IsPostLoadRegistered`
- Simplifies integration with SaveLoadSystem for non-Persist objects

## Key Types
- **PostLoadableClass (Class)**: Base class for objects requiring post-load callbacks

## Key Functions
### PostLoadableClass::On_Post_Load
- Purpose: Virtual hook called after object loading
- Calls: None

### PostLoadableClass::Is_Post_Load_Registered
- Purpose: Checks if object is registered for post-load
- Calls: None

### PostLoadableClass::Set_Post_Load_Registered
- Purpose: Sets post-load registration flag
- Calls: None

## Globals
- None

## Dependencies
- Key includes: None
- External symbols: `SaveLoadSystem` (referenced in comments)
