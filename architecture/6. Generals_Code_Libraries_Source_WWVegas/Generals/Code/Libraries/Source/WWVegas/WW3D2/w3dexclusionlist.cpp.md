# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3dexclusionlist.cpp

## Purpose
Manages a list of excluded names for W3D objects, providing methods to check if a given object should be excluded.

## Responsibilities
- Maintains a hash table of excluded names
- Provides exclusion checks for different W3D object types (prototypes, HTrees, HAnims)
- Handles name parsing and normalization for exclusion checks

## Key Types
- **W3DExclusionListClass (Class)**: Manages exclusion list and provides checking methods
- **DynamicVectorClass<StringClass> (Type)**: Stores list of excluded names
- **HashTableClass<StringClass,int> (Type)**: Maps names to indices for fast lookup

## Key Functions
### W3DExclusionListClass(const DynamicVectorClass<StringClass> & names)
- Purpose: Constructor that initializes the exclusion list
- Calls: NameHash.Insert()

### Is_Excluded(PrototypeClass * proto)
- Purpose: Checks if a prototype is excluded
- Calls: strchr(), Is_Excluded(const char*)

### Is_Excluded(HTreeClass * htree)
- Purpose: Checks if an HTree is excluded
- Calls: Is_Excluded(const char*)

### Is_Excluded(HAnimClass * hanim)
- Purpose: Checks if an HAnim is excluded
- Calls: strchr(), Is_Excluded(const char*)

### Is_Excluded(const char * root_name)
- Purpose: Core exclusion check using the name hash
- Calls: NameHash.Exists()

## Globals
- None

## Dependencies
- w3dexclusionlist.h
- proto.h (PrototypeClass)
- htree.h (HTreeClass)
- hanim.h (HAnimClass)
- StringClass, DynamicVectorClass, HashTableClass
