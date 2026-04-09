# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.h

## Purpose
Manages hierarchical animation (HAnim) resources in the W3D engine, including loading, caching, and tracking missing animations.

## Responsibilities
- Load and cache HAnim assets (compressed, raw, morph)
- Provide access to loaded animations via name lookup
- Track missing animations to avoid repeated failed loads
- Free animation memory with optional exclusion lists
- Support iteration over loaded animations

## Key Types
- **HAnimClass (Class)**: Base class for hierarchical animations (forward declared).
- **ChunkLoadClass (Class)**: Handles chunk-based file loading (forward declared).
- **W3DExclusionListClass (Class)**: Defines animations to exclude during cleanup (forward declared).
- **MissingAnimClass (Class)**: Tracks names of animations that failed to load.
- **HAnimManagerClass (Class)**: Core manager for HAnim resources.
- **HAnimManagerIterator (Class)**: Iterator for traversing loaded animations.

## Key Functions
### Load_Anim
- Purpose: Load an animation from a chunk loader.
- Calls: Load_Compressed_Anim, Load_Raw_Anim, Load_Morph_Anim

### Get_Anim
- Purpose: Retrieve a loaded animation by name.
- Calls: None

### Add_Anim
- Purpose: Add an existing HAnimClass to the manager.
- Calls: None

### Free_All_Anims
- Purpose: Release all loaded animations.
- Calls: None

### Register_Missing
- Purpose: Record a failed animation load attempt.
- Calls: None

### Load_Compressed_Anim
- Purpose: Load a compressed animation chunk.
- Calls: None

### Load_Raw_Anim
- Purpose: Load a raw animation chunk.
- Calls: None

### Load_Morph_
