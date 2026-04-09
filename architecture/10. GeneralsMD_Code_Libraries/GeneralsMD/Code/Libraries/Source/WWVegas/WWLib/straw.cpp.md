# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/straw.cpp

## Purpose
Implements a linked-list data structure (Straw) for chaining data-fetching operations.

## Responsibilities
- Manages linking/delinking of Straw segments in a chain
- Provides base data-fetching interface via Get()
- Handles chain integrity during destruction

## Key Types
- Straw (Class): Base class for chained data-fetching segments

## Key Functions
### Straw::~Straw
- Purpose: Removes segment from chain and maintains chain integrity
- Calls: None

### Straw::Get_From
- Purpose: Connects this segment to another Straw segment
- Calls: None

### Straw::Get
- Purpose: Fetches data by delegating to next segment in chain
- Calls: ChainTo->Get()

## Globals
- None

## Dependencies
- "always.h", "straw.h", <stddef.h>
- Straw class (defined in straw.h)
