# GeneralsMD/Code/Libraries/Source/Compression/EAC/btreecodex.h - Enhanced Analysis

## Architectural Role
This header defines the B-tree compression codec API, part of EA's proprietary EAC compression library. It provides low-level compression/decompression primitives used by the engine's asset pipeline and runtime data handling.

## Cross-References
### Incoming
- Asset loading systems (e.g., W3D model loader, audio streaming)
- Save/load game functionality
- Network serialization for compressed data packets

### Outgoing
- `codex.h` (parent header for codec infrastructure)
- Likely calls into platform-specific memory allocation (via `GCALL`)

## Design Patterns
- **Facade Pattern**: Exposes simplified compression API hiding B-tree implementation details
- **Adapter Pattern**: Provides C and C++ compatible interfaces for cross-language use
- **Dependency Injection**: `opts` parameter allows runtime configuration of compression behavior

*Not inferable*: No clear use of other patterns without implementation details.
