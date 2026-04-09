# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/shapipe.cpp

## Purpose
Implements a pipe segment that computes a SHA digest of data passing through it.

## Responsibilities
- Passes data through without modification
- Computes SHA digest of the data
- Provides access to the current SHA digest

## Key Types
- SHAPipe (Class): A pipe segment that computes SHA digest of data

## Key Functions
### SHAPipe::Put
- Purpose: Passes data through the pipe and updates the SHA digest
- Calls: SHA.Hash, Pipe::Put

### SHAPipe::Result
- Purpose: Retrieves the current SHA digest
- Calls: SHA.Result

## Globals
- None

## Dependencies
- "always.h"
- "shapipe.h"
- SHA (external class)
- Pipe (base class)
