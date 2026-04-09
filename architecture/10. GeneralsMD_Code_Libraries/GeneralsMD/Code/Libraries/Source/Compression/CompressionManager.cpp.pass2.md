# GeneralsMD/Code/Libraries/Source/Compression/CompressionManager.cpp - Enhanced Analysis

## Architectural Role
Central compression/decompression utility used across the engine for asset loading, networking, and save game handling. Acts as a facade for multiple compression algorithms, abstracting their differences.

## Cross-References
### Incoming
- Asset loading pipeline (e.g., W3D model loading)
- Networking layer (packet compression)
- Save/load system
- Map cache (DoCompressTest)

### Outgoing
- External compression libraries (ZLib, EA's custom codecs)
- File system (for test data access)
- Performance timing system (PerfGather)

## Design Patterns
- **Facade Pattern**: Hides complexity of multiple compression algorithms behind a simple interface
- **Strategy Pattern**: Different compression algorithms implemented as separate functions, selected at runtime
- **Singleton-like**: Static-only class with no instance management (implicit singleton)

Rules followed. Output under 400 tokens.
