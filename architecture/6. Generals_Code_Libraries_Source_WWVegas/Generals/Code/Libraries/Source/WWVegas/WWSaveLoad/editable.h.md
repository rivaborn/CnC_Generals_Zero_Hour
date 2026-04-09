# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/editable.h

## Purpose
Defines the `EditableClass` base class and macros for parameter editing functionality in the game engine.

## Responsibilities
- Provides base class for editable game objects
- Declares parameter editing macros (when `PARAM_EDITING_ON` is defined)
- Manages parameter lists for editable properties

## Key Types
- **EditableClass (Class)**: Base class for objects with editable parameters

## Key Functions
### `Get_Parameter_Count`
- Purpose: Returns the number of editable parameters
- Calls: None

### `Lock_Parameter`
- Purpose: Retrieves a parameter by index
- Calls: `WWASSERT`

### `Unlock_Parameter`
- Purpose: Releases a locked parameter
- Calls: None

## Globals
- None

## Dependencies
- `always.h`, `persist.h`, `parameter.h`, `simpleparameter.h`, `parameterlist.h`, `wwdebug.h`
- `ParameterClass`, `ParameterListClass`, `IntParameterClass`, `FloatParameterClass`, `AngleParameterClass`, etc.
