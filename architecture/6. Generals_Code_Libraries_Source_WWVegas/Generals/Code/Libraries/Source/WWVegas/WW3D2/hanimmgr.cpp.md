# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.cpp

## Purpose
Manages hierarchical animation resources (loading, caching, and retrieval) for the W3D engine.

## Responsibilities
- Loads and caches different animation types (raw, compressed, morph)
- Tracks missing animations to avoid repeated disk searches
- Provides reference-counted access to animations
- Supports selective unloading of animations via exclusion lists

## Key Types
- **HAnimManagerClass**: Manages animation resources and loading
- **HAnimManagerIterator**: Iterates over loaded animations
- **MissingAnimClass**: Tracks missing animation names
- **HashTableClass**: Used internally for animation lookup

## Key Functions
### Load_Anim
- Purpose: Dispatches animation loading based on chunk type
- Calls: Load_Raw_Anim, Load_Compressed_Anim, Load_Morph_Anim

### Get_Anim
- Purpose: Returns a reference-counted animation by name
- Calls: Peek_Anim

### Free_All_Anims
- Purpose: Releases all loaded animations
- Calls: HAnimManagerIterator methods

### Add_Anim
- Purpose: Adds an externally created animation to the manager
- Calls: None (direct table manipulation)

## Globals
- **AnimPtrTable** (HashTableClass*): Stores loaded animations
- **MissingAnimTable** (HashTableClass*): Tracks missing animations

## Dependencies
- **hanimmgr.h**: Header for this class
- **hanim.h**, **hrawanim.h**, **hcanim.h**, **hmorphanim.h**: Animation types
- **chunkio.h**: Chunk loading infrastructure
- **wwmemlog.h**: Memory logging
- **w3dexclusionlist.h**: For selective unloading
