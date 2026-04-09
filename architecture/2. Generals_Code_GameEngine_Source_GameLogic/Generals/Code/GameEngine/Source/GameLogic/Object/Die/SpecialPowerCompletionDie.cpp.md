# Generals/Code/GameEngine/Source/GameLogic/Object/Die/SpecialPowerCompletionDie.cpp

## Purpose
This file implements the `SpecialPowerCompletionDie` class, which is responsible for notifying the script engine when a special power has been completed.

## Responsibilities
- Notifies the script engine of completed special powers.
- Manages the creator ID associated with the completion event.
- Handles serialization and deserialization of its state.

## Key Types
- `SpecialPowerCompletionDie` (Class): Manages the notification of special power completions to the script engine.

## Key Functions
### onDie
- Purpose: Checks if the die event is applicable and notifies the script engine if it is.
- Calls: `isDieApplicable`, `notifyScriptEngine`

### notifyScriptEngine
- Purpose: Notifies the script engine about a completed special power.
- Calls: `TheScriptEngine->notifyOfCompletedSpecialPower`

### setCreator
- Purpose: Sets the creator ID for the completion event if not already set.
- Calls: None

## Globals
- None

## Dependencies
- Includes:
  - "Common/Player.h"
  - "Common/SpecialPower.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/SpecialPowerCompletionDie.h"
  - "GameLogic/Object.h"
  - "GameLogic/ScriptEngine.h"
