# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/parameterlist.h

## Purpose
Defines a container class for managing a list of ParameterClass objects, used in save/load functionality.

## Responsibilities
- Maintains a dynamic vector of ParameterClass pointers
- Provides methods to add parameters (by data or existing object)
- Handles cleanup of parameter objects

## Key Types
- **ParameterListClass (Class)**: Container for ParameterClass objects with add/remove functionality

## Key Functions
### ~ParameterListClass
- Purpose: Destructor that frees all parameters
- Calls: Free_Parameters

### Add (void *data, const char *param_name, ParameterClass::Type type)
- Purpose: Creates and adds a new parameter from raw data
- Calls: ParameterClass::Construct, DynamicVectorClass<ParameterClass *>::Add

### Add (ParameterClass *parameter)
- Purpose: Adds an existing parameter object to the list
- Calls: DynamicVectorClass<ParameterClass *>::Add

### Free_Parameters
- Purpose: Deletes all parameter objects and clears the vector
- Calls: delete (on each parameter), m_Parameters.Delete_All

## Globals
- None

## Dependencies
- "always.h", "vector.h", "parameter.h", "wwdebug.h"
- ParameterClass, DynamicVectorClass<ParameterClass *>
- Uses WWASSERT macro
