# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/shastraw.cpp

## Purpose
Implements a "straw" (data processing pipeline) that computes SHA-1 hashes on data passing through it.

## Responsibilities
- Processes data through a SHA-1 hash function
- Provides access to the computed hash digest
- Inherits from a base `Straw` class for data fetching

## Key Types
- `SHAStraw` (Class): SHA-1 processing straw segment
- `SHA` (Member): SHA-1 hash processor instance

## Key Functions
### `SHAStraw::Get`
- Purpose: Fetches data and processes it through SHA-1
- Calls: `Straw::Get`, `SHA.Hash`

### `SHAStraw::Result`
- Purpose: Retrieves the current SHA-1 digest
- Calls: `SHA.Result`

## Globals
- None

## Dependencies
- `always.h`, `shastraw.h`
- `Straw` base class
- `SHA` class (SHA-1 processor)
