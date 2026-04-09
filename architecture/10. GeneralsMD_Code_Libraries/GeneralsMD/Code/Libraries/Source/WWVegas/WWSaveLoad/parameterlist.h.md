# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/parameterlist.h

## Purpose
Manages a dynamic list of ParameterClass objects for save/load operations.

## Responsibilities
- Stores ParameterClass pointers in a DynamicVectorClass
- Provides methods to add parameters (by data or existing object)
- Handles cleanup of parameter objects

## Key Types
- **ParameterListClass (Class)**: Container for ParameterClass objects, inherits from DynamicVectorClass<ParameterClass *>

## Key Functions
### ~ParameterListClass
- Purpose: Destructor that frees all parameters
- Calls: Free_Parameters

### Add (void *data, const char *param_name, ParameterClass::Type type)
- Purpose: Creates and adds a new parameter of specified type
- Calls: ParameterClass::Construct, DynamicVectorClass<ParameterClass *>::Add

### Add (ParameterClass *new_param)
- Purpose: Adds an existing parameter object to the list
- Calls: DynamicVectorClass<ParameterClass *>::Add

### Free_Parameters
- Purpose: Deletes all parameter objects and clears the vector
- Calls: delete (on each parameter), Delete_All

## Globals
None

## Dependencies
- "always.h", "vector.h", "parameter.h", "wwdebug.h"
- DynamicVectorClass<ParameterClass *>
- ParameterClass (external)
