# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.h

## Purpose
Manages hierarchical animation (HAnim) resources in the W3D engine, including loading, caching, and tracking missing animations.

## Responsibilities
- Load and cache HAnim assets (compressed, raw, morph)
- Provide access to loaded animations via name lookup
- Track missing animations to avoid repeated failed loads
- Free animation memory with optional exclusion lists
- Support iteration over loaded animations

## Key Types
- **HAnimClass (Class)**: Base class for hierarchical animations (defined elsewhere)
- **ChunkLoadClass (Class)**: Handles chunk-based file loading (defined elsewhere)
- **W3DExclusionListClass (Class)**: Specifies animations to exclude during cleanup (defined elsewhere)
- **MissingAnimClass (Class)**: Tracks names of animations that failed to load
- **HAnimManagerClass (Class)**: Core manager for animation resources
- **HAnimManagerIterator (Class)**: Iterator for traversing loaded animations

## Key Functions
### Load_Anim
- Purpose: Loads an animation from a chunk loader
- Calls: Load_Compressed_Anim, Load_Raw_Anim, Load_Morph_Anim

### Get_Anim
- Purpose: Retrieves a loaded animation by name
- Calls: None

### Add_Anim
- Purpose: Adds an externally loaded animation to the manager
- Calls: None

### Free_All_Anims
- Purpose: Releases all loaded animations
- Calls: None

### Register_Missing
- Purpose: Records a failed animation load attempt
- Calls: None

### Create_Asset_List
- Purpose: Generates a list of loaded animation assets
- Calls: None

## Globals
- **AnimPtrTable (HashTableClass)**: Stores loaded animations by name
- **MissingAnim
