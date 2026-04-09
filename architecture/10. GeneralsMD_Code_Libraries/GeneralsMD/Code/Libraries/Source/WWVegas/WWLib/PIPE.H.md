# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/PIPE.H

## Purpose
Defines an abstract base class for a data processing pipeline (Pipe) used for compression, translation, or other data transformations.

## Responsibilities
- Provides a virtual interface for chaining data processing stages.
- Manages pipe chaining via `ChainTo` and `ChainFrom` pointers.
- Defines core methods for flushing, ending, and writing data (`Put`).
- Prevents copying via disabled copy constructor and assignment operator.

## Key Types
- **Pipe (Class)**: Abstract base class for data processing pipelines.

## Key Functions
### `Flush`
- Purpose: Flushes buffered data.
- Calls: None (pure virtual).

### `End`
- Purpose: Ends the pipe (calls `Flush` by default).
- Calls: `Flush`.

### `Put_To`
- Purpose: Chains this pipe to another pipe.
- Calls: None.

### `Put`
- Purpose: Writes data into the pipe.
- Calls: None (pure virtual).

## Globals
- None.

## Dependencies
- Key includes: None.
- External symbols: None.
