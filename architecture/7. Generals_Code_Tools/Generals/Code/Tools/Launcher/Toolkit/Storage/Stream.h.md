# Generals/Code/Tools/Launcher/Toolkit/Storage/Stream.h

## Purpose
Defines the abstract base class for data streaming functionality in the SAGE engine.

## Responsibilities
- Declares pure virtual methods for stream operations (read/write/seek).
- Defines stream positioning modes (absolute/relative/from end).
- Serves as interface for concrete stream implementations.

## Key Types
- **Stream (Class)**: Abstract base class for stream operations.
- **EStreamFrom (Enum)**: Stream positioning modes (FromStart, FromMarker, FromEnd).

## Key Functions
### GetLength
- Purpose: Returns the stream length in bytes.
- Calls: None.

### SetLength
- Purpose: Sets the stream length in bytes.
- Calls: None.

### GetMarker
- Purpose: Returns the current stream position.
- Calls: None.

### SetMarker
- Purpose: Sets the stream position relative to a reference point.
- Calls: None.

### AtEnd
- Purpose: Checks if the stream marker is at the end.
- Calls: None.

### GetBytes
- Purpose: Reads bytes from the stream into a buffer.
- Calls: None.

### PutBytes
- Purpose: Writes bytes from a buffer to the stream.
- Calls: None.

### PeekBytes
- Purpose: Reads bytes without advancing the stream marker.
- Calls: None.

### Flush
- Purpose: Flushes any buffered data to the underlying storage.
- Calls: None.

## Globals
None.

## Dependencies
- **Support\UTypes.h**: For UInt32, Int32, and bool types.
