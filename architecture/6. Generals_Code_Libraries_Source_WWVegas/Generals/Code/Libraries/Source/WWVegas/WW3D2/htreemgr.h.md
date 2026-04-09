# Generals/Code/Libraries/Source/WWVegas/WW3D2/htreemgr.h

## Purpose
Manages hierarchy trees (base poses for hierarchy models) in the W3D engine.

## Responsibilities
- Load and track hierarchy trees
- Provide access to trees by name or ID
- Free memory used by trees
- Maintain exclusion lists for selective tree unloading

## Key Types
- **HTreeManagerClass (Class)**: Manages hierarchy trees.
- **MAX_TREES (Enum)**: Maximum number of trees (16000).

## Key Functions
### HTreeManagerClass()
- Purpose: Constructor.
- Calls: None.

### ~HTreeManagerClass()
- Purpose: Destructor.
- Calls: None.

### Load_Tree(ChunkLoadClass & cload)
- Purpose: Loads a hierarchy tree from a chunk loader.
- Calls: Not inferable.

### Get_Tree(const char * name)
- Purpose: Retrieves a tree by name.
- Calls: Not inferable.

### Get_Tree(int id)
- Purpose: Retrieves a tree by ID.
- Calls: Not inferable.

### Free_All_Trees()
- Purpose: Frees all loaded trees.
- Calls: Free().

### Free_All_Trees_With_Exclusion_List(const W3DExclusionListClass & exclusion_list)
- Purpose: Frees trees not in the exclusion list.
- Calls: Not inferable.

### Free()
- Purpose: Internal cleanup method.
- Calls: Not inferable.

## Globals
- **TreePtr[MAX_TREES] (HTreeClass*)**: Array storing tree pointers.

## Dependencies
- `FileClass`, `ChunkLoadClass`, `HTreeClass`, `W3DExclusionListClass` (forward declarations).
- `always.h`, `bittype.h
