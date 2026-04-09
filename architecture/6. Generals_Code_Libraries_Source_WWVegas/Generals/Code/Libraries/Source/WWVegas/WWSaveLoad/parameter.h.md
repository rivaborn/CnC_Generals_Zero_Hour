# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/parameter.h

## Purpose
Defines the ParameterClass hierarchy for game data serialization, including various parameter types for game objects, files, and values.

## Responsibilities
- Declares base ParameterClass and derived classes for different data types
- Defines type enumeration for parameter classification
- Provides RTTI and comparison operators for parameter objects
- Manages parameter names, units, and modification tracking

## Key Types
- ParameterClass (Class): Base class for all parameter types
- DefParameterClass (Class): Base class for definition ID parameters
- (anonymous enum) (Enum): Parameter type enumeration (TYPE_INT, TYPE_FLOAT, etc.)
- StringParameterClass (Class): String parameter specialization
- FilenameParameterClass (Class): File path parameter specialization
- EnumParameterClass (Class): Enumeration parameter specialization
- GameObjDefParameterClass (Class): Game object definition ID parameter
- ScriptParameterClass (Class): Script parameter specialization
- DefIDListParameterClass (Class): List of definition IDs parameter
- ZoneParameterClass (Class): Spatial zone parameter
- SeparatorParameterClass (Class): UI separator parameter

## Key Functions
### Construct
- Purpose: Factory method to create parameter instances by type
- Calls: Not visible in header

### Copy_Value
- Purpose: Virtual method to copy parameter values between instances
- Calls: Varies by derived class

### Get_Type/Is_Type
- Purpose: Type identification methods
- Calls: None

## Globals
- None

## Dependencies
- "always.h", "parametertypes.h", "vector.h", "wwstring.h", "bittype.h", "obbox.h"
- StringClass, DynamicVectorClass, OBBoxClass, uint32
