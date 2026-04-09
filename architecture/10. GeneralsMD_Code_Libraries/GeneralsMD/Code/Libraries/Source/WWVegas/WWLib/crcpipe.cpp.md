# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crcpipe.cpp

## Purpose
Implements a CRC (Cyclic Redundancy Check) calculation pipe for data streams in the SAGE engine.

## Responsibilities
- Calculates CRC for data passing through the pipe
- Provides access to the current CRC result
- Inherits from `Pipe` for data streaming functionality

## Key Types
- `CRCPipe` (Class): A pipe that calculates CRC for data passing through it

## Key Functions
### `CRCPipe::Put`
- Purpose: Retrieves data and calculates CRC on it
- Calls: `CRC`, `Pipe::Put`

### `CRCPipe::Result`
- Purpose: Returns the current CRC value of the data stream
- Calls: `CRC`

## Globals
- None

## Dependencies
- `always.h`
- `crcpipe.h`
- `Pipe` class (base class)
- `CRC` function (inherited or external)
