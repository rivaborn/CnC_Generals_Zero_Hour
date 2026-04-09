# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/CallbackHook.h

## Purpose
Defines a callback mechanism for deferring function execution, used in the SAGE engine for event-driven programming.

## Responsibilities
- Provides base `CallbackHook` class for polymorphic callback handling.
- Implements templated `Callback` class to wrap user-provided functions.
- Manages callback invocation via `DoCallback()`.
- Supports type-safe user data passing.

## Key Types
- **CallbackHook (Class)**: Abstract base class for callback objects.
- **Callback<T> (Class)**: Templated derived class wrapping a user function and data.

## Key Functions
### CallbackHook::DoCallback
- Purpose: Placeholder for callback execution (returns false by default).
- Calls: None.

### Callback::DoCallback
- Purpose: Invokes the stored user function with its data.
- Calls: `mCallback(mUserData)`.

### Callback::Callback (constructor)
- Purpose: Initializes the callback with a function pointer and user data.
- Calls: None.

## Globals
- None.

## Dependencies
- No external includes or symbols. Self-contained header.
