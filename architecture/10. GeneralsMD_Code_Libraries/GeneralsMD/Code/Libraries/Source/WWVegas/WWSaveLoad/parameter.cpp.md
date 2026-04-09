# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/parameter.cpp

## Purpose
Implements parameter classes for the game's editable system, handling various data types like strings, filenames, zones, and lists.

## Responsibilities
- Defines parameter classes for different data types
- Implements constructors, operators, and value copying
- Manages string, filename, zone, and list parameters
- Provides factory method for parameter creation

## Key Types
- **ParameterClass (Class)**: Base class for all parameter types
- **StringParameterClass (Class)**: Handles string parameters
- **FilenameParameterClass (Class)**: Manages filename parameters
- **ZoneParameterClass (Class)**: For zone/OBBox parameters
- **FilenameListParameterClass (Class)**: Manages lists of filenames
- **ScriptListParameterClass (Class)**: Handles script name/parameter lists
- **SeparatorParameterClass (Class)**: Represents separators in parameter lists

## Key Functions
### ParameterClass::Construct
- Purpose: Factory method to create parameter instances of specific types
- Calls: Constructors for various parameter subclasses

### StringParameterClass::Copy_Value
- Purpose: Copies string value from another parameter
- Calls: ParameterClass::Copy_Value

### ZoneParameterClass::operator==
- Purpose: Compares two zone parameters for equality
- Calls: OBBoxClass comparison operator

### FilenameListParameterClass::operator==
- Purpose: Compares two filename lists for equality
- Calls: StringClass comparison via stricmp

## Globals
None

## Dependencies
- parameter.h
- parametertypes.h
- simpleparameter.h
- wwstring.h
- definitionclassids.h
- DynamicVectorClass
- OBBoxClass
- StringClass
- W3DNEW macro
