# Generals/Code/Libraries/Source/WWVegas/WWLib/PIPE.H

## Purpose
Defines an abstract base class for data processing pipelines (e.g., compression, translation).

## Responsibilities
- Provides a chaining mechanism for data processing stages
- Defines core methods for data input/output
- Prevents copying via disabled copy constructor/assignment
- Manages pipe segment connections (ChainTo/ChainFrom)

## Key Types
- Pipe (Class): Abstract base class for data processing pipelines

## Key Functions
### Pipe()
- Purpose: Default constructor initializing chain pointers
- Calls: None

### ~Pipe()
- Purpose: Virtual destructor
- Calls: None

### Flush()
- Purpose: Flushes buffered data
- Calls: None

### End()
- Purpose: Ends processing (calls Flush)
- Calls: Flush()

### Put_To()
- Purpose: Sets the next pipe in the chain
- Calls: None

### Put()
- Purpose: Writes data to the pipe
- Calls: None

## Globals
- None

## Dependencies
- Key includes: None
- External symbols: None
