# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.cpp

## Purpose
Manages hierarchical animation resources (HAnim) in the W3D engine, handling loading, caching, and retrieval of animation data.

## Responsibilities
- Loads and caches different types of animations (raw, compressed, morph)
- Provides access to animations via name lookup
- Manages memory for loaded animations
- Tracks missing animations to avoid repeated failed lookups
- Supports exclusion-based cleanup of animations

## Key Types
- **HAnimManagerClass**: Main animation manager class
- **HAnimManagerIterator**: Iterator for traversing loaded animations
- **MissingAnimClass**: Tracks names of missing animations
- **HashTableClass**: Used internally for animation storage

## Key Functions
### Load_Anim
- Purpose: Dispatches loading of animations based on chunk type
- Calls: Load_Raw_Anim, Load_Compressed_Anim, Load_Morph_Anim

### Get_Anim
- Purpose: Retrieves an animation by name with reference counting
- Calls: Peek_Anim

### Free_All_Anims
- Purpose: Releases all loaded animations
- Calls: HAnimManagerIterator operations

### Add_Anim
- Purpose: Adds an externally created animation to the manager
- Calls: None (direct operations)

### Register_Missing
- Purpose: Records failed animation lookups to avoid repeats
- Calls: None

## Globals
- **AnimPtrTable** (HashTableClass): Stores loaded animations
- **MissingAnimTable** (HashTableClass): Stores names of missing animations

## Dependencies
- **hanim.h**, **hrawanim.h**, **hcanim.h**, **hmorphanim.h**: Animation class definitions
- **chunkio.h**: Chunk loading infrastructure
- **wwmemlog.h**: Memory logging
- **w3dexclusionlist.h**: Exclusion list support
- **animatedsoundmgr.h**: Likely for sound integration with animations
