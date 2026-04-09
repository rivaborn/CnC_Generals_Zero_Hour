# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/parameter.h

## Purpose
Defines the parameter system for game data serialization, including various parameter types and their base class hierarchy.

## Responsibilities
- Declares the base `ParameterClass` and its derived classes for different data types
- Defines parameter types (enums) for game data serialization
- Provides virtual methods for parameter manipulation and comparison
- Supports RTTI (Run-Time Type Information) for parameter classes

## Key Types
- **ParameterClass (Class)**: Base class for all parameter types
- **Type (Enum)**: Enumeration of supported parameter types (e.g., `TYPE_INT`, `TYPE_STRING`, `TYPE_VECTOR3`)
- **StringParameterClass (Class)**: Parameter class for string values
- **FilenameParameterClass (Class)**: Parameter class for file paths
- **TextureFilenameParameterClass (Class)**: Parameter class for texture file paths
- **SoundFilenameParameterClass (Class)**: Parameter class for sound file paths
- **EnumParameterClass (Class)**: Parameter class for enumerated values
- **DefParameterClass (Class)**: Base class for definition ID parameters
- **GameObjDefParameterClass (Class)**: Parameter class for game object definition IDs
- **ScriptParameterClass (Class)**: Parameter class for script references
- **DefIDListParameterClass (Class)**: Parameter class for lists of definition IDs
- **ZoneParameterClass (Class)**: Parameter class for zone/area definitions
- **FilenameListParameterClass (Class)**: Parameter class for lists of file paths
- **ScriptListParameterClass (Class)**: Parameter class for lists of scripts
- **SeparatorParameterClass (Class)**: Parameter class for UI separators

## Key Functions
### Construct
- Purpose: Creates a new instance of a parameter type
- Calls: Not inferable (implementation not shown)

### Copy_Value
- Purpose: Copies the value from another parameter
- Calls: Not inferable (implementation not shown)

## Globals
- None

## Dependencies
- `always.h`, `stdlib.h`, `string.h`
- `parametertypes.h`, `vector.h`, `wwstring.h`, `bittype.h`, `obbox.h`
- `DynamicVectorClass`, `StringClass`, `OBBoxClass`
