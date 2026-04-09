# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/editable.h

## Purpose
Defines the `EditableClass` interface and macros for parameter-based object editing in the SAGE engine.

## Responsibilities
- Declares the `EditableClass` base class for editable objects
- Provides macros for registering editable parameters (int, float, string, etc.)
- Supports conditional compilation for parameter editing features

## Key Types
- **EditableClass (Class)**: Base class for objects supporting parameter editing

## Key Functions
### EditableClass::Get_Parameter_Count
- Purpose: Returns the number of editable parameters
- Calls: None

### EditableClass::Lock_Parameter
- Purpose: Retrieves a parameter by index
- Calls: `WWASSERT`

### EditableClass::Unlock_Parameter
- Purpose: Releases a locked parameter
- Calls: None

## Globals
- None

## Dependencies
- `always.h`, `persist.h`, `parameter.h`, `simpleparameter.h`, `parameterlist.h`, `wwdebug.h`
- `ParameterClass`, `ParameterListClass`, `IntParameterClass`, `FloatParameterClass`, etc. (from included headers)
