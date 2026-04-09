# GeneralsMD/Code/Libraries/Source/Compression/EAC/refdecode.cpp - Enhanced Analysis

## Architectural Role
This file implements the core decompression logic for EAC (Electronic Arts Compression) format, serving as a critical component in the game's asset loading pipeline. It handles the low-level decoding of compressed data, which is essential for efficiently loading game resources like textures, models, and audio.

## Cross-References
### Incoming
- Likely called by asset loading systems (e.g., W3D model loader, texture manager)
- Potentially used by modding infrastructure for custom asset decompression

### Outgoing
- Depends on `ggetm` from `codex.h`/`refcodex.h` for multi-byte reads
- No other subsystem dependencies (self-contained decompression logic)

## Design Patterns
- **Data Access Object (DAO)**: Encapsulates decompression logic behind simple functions (`REF_is`, `REF_size`, `REF_decode`)
- **Command Pattern**: Each function represents a self-contained operation on compressed data
- **Not inferable**: No clear use of other patterns (e.g., no factory, observer, or strategy patterns visible)

*Token count: 198*
