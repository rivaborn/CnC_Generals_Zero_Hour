# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/htreemgr.h

## Purpose
Manages hierarchy trees (base poses for hierarchy models) in the W3D engine.

## Responsibilities
- Load and track hierarchy trees
- Provide access to trees by name or ID
- Free memory used by trees
- Maintain a hash-based lookup system

## Key Types
- **HTreeManagerClass (Class)**: Manages hierarchy trees.
- **MAX_TREES (Enum)**: Defines maximum tree capacity (16000).

## Key Functions
### HTreeManagerClass()
- Purpose: Constructor.
- Calls: Not inferable.

### Load_Tree()
- Purpose: Loads a hierarchy tree from a chunk loader.
- Calls: Not inferable.

### Get_Tree()
- Purpose: Retrieves a tree by name or ID.
- Calls: Not inferable.

### Free_All_Trees()
- Purpose: Frees all loaded trees.
- Calls: Not inferable.

### Free_All_Trees_With_Exclusion_List()
- Purpose: Frees trees excluding those in the exclusion list.
- Calls: Not inferable.

### Free()
- Purpose: Internal cleanup method.
- Calls: Not inferable.

## Globals
- **TreePtr[MAX_TREES] (HTreeClass*)**: Array storing tree pointers.
- **TreeHash (HashTemplateClass)**: Hash table for fast tree lookup.

## Dependencies
- `always.h`, `bittype.h`, `hashtemplate.h`
- `FileClass`, `ChunkLoadClass`, `HTreeClass`, `W3DExclusionListClass`, `StringClass`
