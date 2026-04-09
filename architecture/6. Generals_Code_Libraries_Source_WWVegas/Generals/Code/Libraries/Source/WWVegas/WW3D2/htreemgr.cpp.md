# Generals/Code/Libraries/Source/WWVegas/WW3D2/htreemgr.cpp

## Purpose
Manages hierarchy trees (HTrees) used in the W3D rendering system, including loading, retrieval, and cleanup.

## Responsibilities
- Load and manage HTree objects
- Provide lookup by name or ID
- Free memory when trees are no longer needed
- Support exclusion lists for selective cleanup

## Key Types
- **HTreeManagerClass (Class)**: Manages a collection of HTree objects
- **HTreeClass (Class)**: Represents a hierarchy tree (external, defined in htree.h)

## Key Functions
### HTreeManagerClass::Load_Tree
- Purpose: Loads a hierarchy tree from a chunk file
- Calls: HTreeClass::Load_W3D, W3DNEW, delete

### HTreeManagerClass::Get_Tree_ID
- Purpose: Returns the ID of a named hierarchy tree
- Calls: stricmp

### HTreeManagerClass::Get_Tree
- Purpose: Retrieves a hierarchy tree by name or ID
- Calls: stricmp

### HTreeManagerClass::Free_All_Trees_With_Exclusion_List
- Purpose: Frees all trees not in the exclusion list
- Calls: W3DExclusionListClass::Is_Excluded, delete

## Globals
- **TreePtr[MAX_TREES] (HTreeClass**)**: Array storing loaded HTree objects
- **NumTrees (int)**: Count of currently loaded trees

## Dependencies
- htree.h (HTreeClass)
- chunkio.h (ChunkLoadClass)
- wwmemlog.h (WWMEMLOG)
- w3dexclusionlist.h (W3DExclusionListClass)
- string.h (stricmp)
