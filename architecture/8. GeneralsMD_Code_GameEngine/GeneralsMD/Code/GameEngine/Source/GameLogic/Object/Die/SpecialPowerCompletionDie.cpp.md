# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/SpecialPowerCompletionDie.cpp

## Purpose
Handles notifying the script engine when a special power is completed upon an object's destruction.

## Responsibilities
- Tracks the creator of the special power
- Notifies script engine when object dies
- Serializes/deserializes state for networking

## Key Types
- SpecialPowerCompletionDie (Class): Die module for special power completion events

## Key Functions
### SpecialPowerCompletionDie::onDie
- Purpose: Handles die event and notifies script engine if applicable
- Calls: isDieApplicable, notifyScriptEngine

### SpecialPowerCompletionDie::notifyScriptEngine
- Purpose: Sends completion notification to script engine
- Calls: TheScriptEngine->notifyOfCompletedSpecialPower

### SpecialPowerCompletionDie::setCreator
- Purpose: Sets the creator ID for the special power
- Calls: None

### SpecialPowerCompletionDie::xfer
- Purpose: Serializes/deserializes object state
- Calls: DieModule::xfer, xfer->xferObjectID, xfer->xferBool

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Player.h
- Common/SpecialPower.h
- Common/Xfer.h
- GameLogic/Module/SpecialPowerCompletionDie.h
- GameLogic/Object.h
- GameLogic/ScriptEngine.h
