# GeneralsMD/Code/GameEngine/Source/GameLogic/ScriptEngine/Scripts.cpp

## Purpose
Manages script data structures, serialization, and UI interaction signals for the game's scripting system.

## Responsibilities
- Defines script list, group, action, and condition classes
- Handles serialization/deserialization of script data
- Manages UI interaction hooks and signal propagation
- Provides script duplication and qualification utilities
- Maintains version compatibility for script data formats

## Key Types
- ScriptList (Class): Container for script groups and scripts
- ScriptGroup (Class): Group of related scripts
- ScriptAction (Class): Action to be performed in a script
- ScriptCondition (Class): Condition to evaluate in a script
- Parameter (Class): Script parameter container
- (anonymous enum): Version constants for script data formats

## Key Functions
### SignalUIInteraction
- Purpose: Signals UI interactions to the script engine
- Calls: TheScriptEngine->signalUIInteract

### ScriptList::xfer
- Purpose: Serializes/deserializes script list data
- Calls: Xfer methods on child scripts and groups

### ScriptAction::ParseAction
- Purpose: Parses action data from chunk input
- Calls: Parameter::ReadParameter, TheScriptEngine->getActionTemplate

### ScriptAction::WriteActionDataChunk
- Purpose: Writes action data to chunk output
- Calls: ActionTemplate methods, Parameter::WriteParameter

## Globals
- s_mtScript (Script*): Temporary script instance for recovery
- s_mtGroup (ScriptGroup*): Temporary group instance for recovery
- TheShellHookNames (char**): Array of UI interaction hook names
- Surfaces (const char**): Surface type strings
- ShakeIntensities (const char**): Camera shake intensity strings
- ParameterChangesVer2 (Condition::ConditionType*): List of conditions changed in v2
- TheObjectFlagsNames (const char**): Object flag names

## Dependencies
- Common/GameState.h, Common/Xfer.h, GameLogic/ScriptEngine.h
- GameClient/ShellHooks.h, GameLogic/Ai.h, GameLogic/Object.h
- Common/DataChunk.h, Common/ThingTemplate.h, Common/Player.h
- GameLogic/SidesList.h, GameLogic/Module/ContainModule.h
