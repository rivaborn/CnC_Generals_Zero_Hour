# Generals/Code/Libraries/Source/WWVegas/WWLib/straw.cpp

## Purpose
Implements a linked-list data structure (Straw) for chaining data-fetching operations.

## Responsibilities
- Manages straw segment linking/unlinking
- Provides chained data retrieval
- Handles straw chain integrity during destruction

## Key Types
- Straw (Class): Base class for chained data-fetching segments

## Key Functions
### Straw::~Straw
- Purpose: Destructor that maintains chain integrity when removing a segment
- Calls: None

### Straw::Get_From
- Purpose: Connects this straw segment to another in the chain
- Calls: None

### Straw::Get
- Purpose: Fetches data by delegating to the next segment in the chain
- Calls: Straw::Get (recursively)

## Globals
- None

## Dependencies
- "always.h", "straw.h", <stddef.h>
- Uses Straw class defined in straw.h
