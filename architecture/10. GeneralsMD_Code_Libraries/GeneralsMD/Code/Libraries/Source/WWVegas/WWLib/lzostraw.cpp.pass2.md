# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzostraw.cpp - Enhanced Analysis

## Architectural Role
This file implements the LZOStraw class, which serves as a streaming compression/decompression layer for the SAGE engine. It bridges the low-level LZO library with the engine's resource loading pipeline, enabling efficient handling of compressed assets during runtime.

## Cross-References
### Incoming
- Resource loading systems (e.g., W3D model loader, audio streaming) likely instantiate LZOStraw for decompressing assets
- File I/O abstractions (Straw class) feed compressed data into LZOStraw::Get()

### Outgoing
- Directly calls LZO library functions (lzo1x_decompress/lzo1x_1_compress)
- Uses Straw base class for underlying data source abstraction
- Relies on standard memory operations (memmove, new/delete)

## Design Patterns
- **Adapter Pattern**: Wraps LZO library functions with a cleaner interface for the engine
- **Streaming Pattern**: Processes data in configurable block sizes to balance memory usage and performance
- **Resource Management**: Explicit buffer allocation/deallocation in constructor/destructor (pre-C++11 RAII)

*Not inferable*: No clear use of Factory, Observer, or other patterns from the provided code.
