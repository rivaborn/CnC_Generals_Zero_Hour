# Generals/Code/Tools/Autorun/CallbackHook.h

## Purpose
Defines a callback mechanism for deferred function execution using a base class and a templated derived class.

## Responsibilities
- Provides a base `CallbackHook` class for polymorphic callback handling.
- Implements a templated `Callback` class to wrap user-provided functions and data.
- Supports virtual function dispatch for callbacks.
- Manages lifetime of callback objects.

## Key Types
- **CallbackHook (Class)**: Abstract base class for callback objects.
- **Callback (Class)**: Templated derived class that stores a function pointer and user data.

## Key Functions
### CallbackHook::DoCallback
- Purpose: Placeholder for callback execution (returns false by default).
- Calls: None.

### Callback::DoCallback
- Purpose: Invokes the stored function with user data.
- Calls: `mCallback(mUserData)`.

## Globals
- None.

## Dependencies
- None (header-only, no external includes).
