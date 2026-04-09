# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pipe.cpp

## Purpose
Implements a pipe data structure for chaining data flow between objects.

## Responsibilities
- Manages pipe chaining (linking pipes together)
- Handles data flow through connected pipes
- Ensures proper cleanup and flushing on destruction
- Provides methods for putting data and flushing buffers

## Key Types
- Pipe (Class): Base pipe class for chaining data flow

## Key Functions
### Pipe::~Pipe
- Purpose: Destructor that unlinks the pipe and flushes pending data
- Calls: ChainTo->ChainFrom assignment, ChainFrom->Put_To

### Pipe::Put_To
- Purpose: Connects this pipe to another pipe for data flow
- Calls: ChainFrom->Put_To, ChainTo->ChainFrom assignment

### Pipe::Put
- Purpose: Feeds data through the pipe chain
- Calls: ChainTo->Put (recursive)

### Pipe::Flush
- Purpose: Flushes all pending data through the pipe chain
- Calls: ChainTo->Flush (recursive)

## Globals
None

## Dependencies
- pipe.h (header)
- always.h (header)
- stddef.h (header)
