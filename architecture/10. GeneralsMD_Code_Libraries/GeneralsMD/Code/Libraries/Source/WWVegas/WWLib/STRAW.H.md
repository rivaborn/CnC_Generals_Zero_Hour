# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/STRAW.H

## Purpose
Defines the `Straw` class, a demand-driven data carrier that processes data through a chain of pipes.

## Responsibilities
- Manages data flow through a chain of `Straw` objects.
- Provides virtual methods for data retrieval and chaining.
- Disables copy/assignment to enforce single ownership.

## Key Types
- **Straw (Class)**: Base class for demand-driven data processing pipes.

## Key Functions
### `Get_From(Straw * pipe)`
- Purpose: Sets the next pipe in the chain.
- Calls: None.

### `Get(void * buffer, int slen)`
- Purpose: Retrieves data into the provided buffer.
- Calls: None.

## Globals
- None.

## Dependencies
- Key includes: None.
- External symbols: None.
