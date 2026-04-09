# GeneralsMD/Code/GameEngine/Include/GameLogic/Scripts.h

## Purpose
Defines core scripting data structures for the game engine, including scripts, actions, conditions, and parameters.

## Responsibilities
- Declares classes for script logic (Script, ScriptAction, Condition, Parameter)
- Defines enums for action/condition types and parameter types
- Provides data chunk I/O for serialization
- Manages script groups and lists
- Supports script qualification and duplication

## Key Types
- **ScriptGroup (Class)**: Groups named scripts with activation properties
- **ScriptAction (Class)**: Represents executable script actions with parameters
- **Condition (Class)**: Represents conditional logic with parameters
- **Parameter (Class)**: Stores script parameters of various types
- **ScriptList (Class)**: Container for top-level scripts and groups
- **ScriptActionType (Enum)**: All possible script action types (150+ values)
- **ConditionType (Enum)**: All possible condition types (100+ values)
- **ParameterType (Enum)**: All parameter data types (40+ values)

## Key Functions
### ScriptGroup::duplicateAndQualify
- Purpose: Creates a qualified copy of a script group
- Calls: Not inferable

### ScriptAction::WriteParameter
- Purpose: Serializes a parameter to a data chunk
- Calls: Not inferable

### Condition::getUiText
- Purpose: Returns user-visible text for the condition
- Calls: Not inferable

### ScriptList::ParseScriptsDataChunk
- Purpose: Deserializes scripts from a data chunk
- Calls: Not inferable

## Globals
- **Surfaces (const char**)**: Surface type names
- **ShakeIntensities (const char**)**: Camera shake intensity names
- **TheObjectFlagsNames (const char**)**: Object flag names

## Dependencies
- Common/Snapshot.h
- GameNetwork/NetworkDefs.h
- Common/ObjectStatusTypes.h
- MemoryPoolObject (base class)
- AsciiString, Coord3D, Bool, Int, Real, UnsignedInt
- Xfer, DataChunkInput, DataChunkOutput, DataChunkInfo
