# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/htreemgr.cpp

## Purpose
Manages hierarchy trees (HTrees) used in the W3D rendering system, handling loading, retrieval, and memory management.

## Responsibilities
- Load and manage hierarchy trees from files
- Provide access to trees by name or ID
- Free memory used by trees, with optional exclusion lists
- Maintain a hash table for fast name-based lookups

## Key Types
- **HTreeManagerClass (Class)**: Manages a collection of HTreeClass objects
- **HTreeClass (Class)**: Represents a hierarchy tree (used but defined elsewhere)

## Key Functions
### HTreeManagerClass::Load_Tree
- Purpose: Loads a hierarchy tree from a ChunkLoadClass stream
- Calls: HTreeClass::Load_W3D, Get_Tree_ID, TreeHash.Insert

### HTreeManagerClass::Free_All_Trees_With_Exclusion_List
- Purpose: Frees all trees not in the exclusion list
- Calls: W3DExclusionListClass::Is_Excluded, TreeHash.Remove_All, TreeHash.Insert

### HTreeManagerClass::Get_Tree
- Purpose: Retrieves a tree by name or ID
- Calls: TreeHash.Get

## Globals
- **TreePtr[MAX_TREES] (HTreeClass**)**: Array storing loaded trees
- **NumTrees (int)**: Count of loaded trees
- **TreeHash (HashTableClass)**: Hash table for name-based lookups

## Dependencies
- **htreemgr.h**: Header for HTreeManagerClass
- **htree.h**: Header for HTreeClass
- **chunkio.h**: For ChunkLoadClass
- **wwmemlog.h**: Memory logging
- **w3dexclusionlist.h**: For exclusion list handling
- **string.h**: For string operations
- **HashTableClass**: Used for TreeHash (defined elsewhere)
