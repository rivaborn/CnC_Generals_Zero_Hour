# GeneralsMD/Code/Libraries/Source/Compression/LZHCompress/NoxCompress.h - Enhanced Analysis

## Architectural Role
This header defines the core compression/decompression API used across the engine for both file and memory operations. It serves as the bridge between the game's data handling systems and the underlying LZH compression library, supporting both persistent storage (files) and runtime operations (memory/packets).

## Cross-References
### Incoming
- **File I/O Subsystem**: Uses `CompressFile`/`DecompressFile` for saving/loading compressed assets (e.g., maps, rules).
- **Networking Layer**: Uses `CompressPacket`/`DecompressPacket` for bandwidth optimization in multiplayer.
- **Resource Manager**: Likely calls `CompressMemory`/`DecompressMemory` for dynamic asset compression.
- **Modding Tools**: May use these APIs for packaging mod content with `.nxz` extensions.

### Outgoing
- **LZH Compression Library**: Directly interfaces with the underlying compression implementation (not shown in header).
- **File System Abstraction**: Relies on OS/file APIs for `CompressFile`/`DecompressFile` operations.

## Design Patterns
- **Facade Pattern**: Abstracts the complexity of LZH compression behind simple, high-level functions.
- **Separation of Concerns**: Cleanly separates file, memory, and packet operations, allowing subsystems to use only what they need.
- **Extension-Based Polymorphism**: Uses file extensions (`.nxz`, `.map`) to implicitly determine compression behavior.
