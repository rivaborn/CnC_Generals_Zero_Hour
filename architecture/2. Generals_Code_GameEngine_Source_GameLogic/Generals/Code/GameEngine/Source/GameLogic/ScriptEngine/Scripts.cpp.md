# Generals/Code/GameEngine/Source/GameLogic/ScriptEngine/Scripts.cpp

## Purpose
This file contains the implementation for script handling in Command & Conquer Generals, including classes and functions for managing scripts, script groups, actions, and conditions.

## Responsibilities
- Manage script lists and their serialization.
- Handle UI interactions through scripting hooks.
- Define constants and enums for script versions and types.
- Implement duplication and qualification of scripts for different contexts.

## Key Types
- **ScriptList**: Manages a list of scripts and script groups.
- **ScriptGroup**: Represents a group of scripts.
- **ScriptAction**: Represents an action within a script, with parameters.
- **Condition**: Represents conditions that can trigger actions.

## Key Functions
### SignalUIInteraction
- Purpose: Signals UI interactions to the script engine.
- Calls: TheScriptEngine->signalUIInteract

### ScriptList::updateDefaults
- Purpose: Ensures default scripts are present for each side in the game.

### ScriptList::duplicate
- Purpose: Creates a deep copy of a script list.

### ScriptAction::setActionType
- Purpose: Sets the action type and initializes parameters accordingly.

### ScriptAction::WriteActionDataChunk
- Purpose: Writes an action chunk to a data stream.

## Globals
- **s_mtScript**: Static pointer to a script.
- **s_mtGroup**: Static pointer to a script group.
- **TheShellHookNames**: Array of UI interaction hook names.
- **Surfaces**: Array of surface types.
- **ShakeIntensities**: Array of shake intensity levels.
- **ParameterChangesVer2**: Array of condition types for parameter changes.

## Dependencies
- Includes headers from Common, GameClient, GameLogic, and other modules.
- Uses classes like ScriptEngine, Object, Ai, and Xfer.
