# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3dexclusionlist.h

## Purpose
Defines a class for managing exclusion lists used by the asset manager to filter resources during level transitions.

## Responsibilities
- Stores a list of resource names to exclude
- Provides methods to check if a resource should be excluded
- Uses hashing for efficient lookups

## Key Types
- **W3DExclusionListClass (Class)**: Manages exclusion lists for W3D resources
- **PrototypeClass (Class)**: Reference to a W3D prototype (external)
- **HTreeClass (Class)**: Reference to a W3D hierarchy tree (external)
- **HAnimClass (Class)**: Reference to a W3D animation (external)

## Key Functions
### W3DExclusionListClass(const DynamicVectorClass<StringClass> & names)
- Purpose: Constructor that initializes the exclusion list with a vector of names
- Calls: Not inferable

### Is_Excluded(PrototypeClass * proto)
- Purpose: Checks if a prototype is in the exclusion list
- Calls: Not inferable

### Is_Excluded(HTreeClass * htree)
- Purpose: Checks if a hierarchy tree is in the exclusion list
- Calls: Not inferable

### Is_Excluded(HAnimClass * hanim)
- Purpose: Checks if an animation is in the exclusion list
- Calls: Not inferable

### Is_Excluded(const char * root_name)
- Purpose: Checks if a resource name is in the exclusion list
- Calls: Not inferable

## Globals
- **Names (DynamicVectorClass<StringClass> &)**: Reference to the list of excluded names
- **NameHash (HashTemplateClass<StringClass,int>)**: Hash table for efficient name lookups

## Dependencies
- `always.h
