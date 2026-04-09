# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/parameter.cpp

## Purpose
Implements parameter classes for the game's editable system, handling various data types like strings, vectors, and game object definitions.

## Responsibilities
- Defines parameter classes for different data types (int, float, vector, etc.)
- Implements factory method `Construct()` to create parameter instances
- Provides equality comparison and value copying for parameters
- Manages string-based parameters (String, Filename, SoundFilename)
- Handles complex parameters (Zone, FilenameList, ScriptList)

## Key Types
- **ParameterClass (Class)**: Base class for all parameter types
- **StringParameterClass (Class)**: Handles string parameter storage and comparison
- **FilenameParameterClass (Class)**: Specialized string parameter for filenames
- **ZoneParameterClass (Class)**: Manages OBBox-based zone parameters
- **FilenameListParameterClass (Class)**: Handles lists of filenames
- **ScriptListParameterClass (Class)**: Manages pairs of script name/parameter lists
- **SeparatorParameterClass (Class)**: Represents UI separators in parameter lists

## Key Functions
### ParameterClass::Construct
- Purpose: Factory method to create parameter instances based on type
- Calls: Constructors for specific parameter subclasses (IntParameterClass, FloatParameterClass, etc.)

### StringParameterClass::Copy_Value
- Purpose: Copies string value from another parameter
- Calls: ParameterClass::Copy_Value

### ZoneParameterClass::operator==
- Purpose: Compares two zone parameters for equality
- Calls: OBBoxClass comparison operator

### FilenameListParameterClass::operator==
- Purpose: Compares two filename lists for equality
- Calls: DynamicVectorClass methods and string comparison

## Globals
None

## Dependencies
- Key includes: "parameter.h", "parametertypes.h", "simpleparameter.h", "wwstring.h", "definitionclassids.h"
- External symbols: W3DNEW, DynamicVectorClass, StringClass, OBBoxClass, CLASSID_GAME_OBJECTS
