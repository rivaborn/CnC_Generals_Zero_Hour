# Generals/Code/Tools/matchbot/wlib/threadsafe.h

## Purpose
This file enforces thread-safety by preventing compilation when non-thread-safe functions are used in a multi-threaded context.

## Responsibilities
- Blocks usage of non-thread-safe C standard library functions
- Acts as a compile-time safety check for multi-threaded code
- Provides clear error messages for unsafe function calls

## Key Types
None

## Key Functions
None

## Globals
None

## Dependencies
- Uses `_REENTRANT` macro to control activation
- Defines `THREADSAFE_HEADER` guard
- No external symbols used
