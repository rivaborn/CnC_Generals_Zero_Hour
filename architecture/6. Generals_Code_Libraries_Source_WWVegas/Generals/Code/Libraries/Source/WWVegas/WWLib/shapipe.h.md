# Generals/Code/Libraries/Source/WWVegas/WWLib/shapipe.h

## Purpose
Defines a pipe class that computes a Secure Hash Algorithm (SHA) hash of data flowing through it.

## Responsibilities
- Inherits from `Pipe` to process data streams.
- Computes SHA hash incrementally via `Put()`.
- Provides access to the final hash via `Result()`.
- Prevents copying via private copy constructor/assignment.

## Key Types
- **SHAPipe (Class)**: A pipe that generates SHA hashes from data streams.

## Key Functions
### SHAPipe::Put
- Purpose: Processes input data and updates the SHA hash incrementally.
- Calls: `SHAEngine` methods (not visible in header).

### SHAPipe::Result
- Purpose: Retrieves the computed SHA hash into a caller-provided buffer.
- Calls: `SHAEngine` methods (not visible in header).

## Globals
- None

## Dependencies
- `pipe.h` (base class `Pipe`)
- `sha.h` (`SHAEngine` class)
