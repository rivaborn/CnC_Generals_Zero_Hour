# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3dexclusionlist.cpp

## Purpose
Manages a list of excluded 3D model components (prototypes, HTrees, HAnims) for rendering purposes.

## Responsibilities
- Stores names of excluded components in a hash table.
- Provides methods to check if a component should be excluded.
- Handles name parsing for sub-objects and munged prototypes.

## Key Types
- **W3DExclusionListClass (Class)**: Manages exclusion list and checks.
- **DynamicVectorClass<StringClass> (Type)**: Container for exclusion names.
- **HashTableClass<StringClass, int> (Type)**: Maps names to indices.

## Key Functions
### W3DExclusionListClass(const DynamicVectorClass<StringClass> & names)
- Purpose: Constructor initializes exclusion list from provided names.
- Calls: `NameHash.Insert()`

### Is_Excluded(PrototypeClass * proto)
- Purpose: Checks if a prototype is excluded, handling sub-objects and munged names.
- Calls: `strchr()`, `Is_Excluded(const char *)`

### Is_Excluded(HTreeClass * htree)
- Purpose: Checks if an HTree is excluded by its name.
- Calls: `Is_Excluded(const char *)`

### Is_Excluded(HAnimClass * hanim)
- Purpose: Checks if an HAnim is excluded, using the name after the dot.
- Calls: `strchr()`, `Is_Excluded(const char *)`

### Is_Excluded(const char * root_name)
- Purpose: Core exclusion check using the hash table.
- Calls: `NameHash.Exists()`

## Globals
None

## Dependencies
- `w3dexclusionlist.h`, `proto.h`, `htree.h`, `hanim.h`
- `
