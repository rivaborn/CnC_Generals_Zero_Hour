# Generals/Code/Libraries/Source/WWVegas/WWLib/IFF.H - Enhanced Analysis

## Architectural Role
This header bridges the engine's asset loading pipeline and Westwood's proprietary IFF format handling. It exposes compression/decompression primitives and IFF chunk I/O, serving as the low-level interface for game assets (images, data chunks) while abstracting platform-specific details (e.g., endianness via `IFFize_WORD/Long`).

## Cross-References
### Incoming
- **Asset Loading**: `LOAD.CPP` (uses `Load_Data`, `Load_Uncompress`)
- **Rendering**: `LOADPICT.CPP` (image loading via `Load_Picture`)
- **File I/O**: `WRITELBM.CPP` (LBM file writing)
- **Assembly**: `PACK2PLN.ASM`, `LCWCOMP.ASM`, `LCWUNCMP.ASM` (compression routines)

### Outgoing
- **Buffer Management**: `BufferClass` (from `buff.h`) for scratch/destination buffers
- **File System**: Low-level file handles (e.g., `Open_Iff_File`)

## Design Patterns
- **Facade Pattern**: Hides IFF format complexity (chunking, compression) behind simple APIs like `Read_Iff_Chunk`.
- **Strategy Pattern**: Compression methods (`CompressionType`) are interchangeable via the `Method` field in `CompHeaderType`.
- **Assembly Integration**: Uses `extern "C"` to expose assembly-optimized routines (`LCW_Compress/Uncompress`) for performance-critical paths.
