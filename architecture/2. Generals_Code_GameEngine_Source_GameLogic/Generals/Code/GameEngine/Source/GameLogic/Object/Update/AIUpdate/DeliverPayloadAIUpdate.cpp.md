# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/DeliverPayloadAIUpdate.cpp

## Purpose
This file implements the `DeliverPayloadAIUpdate` class, which manages the AI logic for delivering payloads by airborne units in Command & Conquer Generals. It handles state transitions, payload delivery, and various behaviors like diving and strafing.

## Responsibilities
- Manages the state machine for payload delivery.
- Handles payload deployment logic, including positioning and timing.
- Implements diving and strafing behavior for aircraft delivering payloads.
- Ensures proper cleanup of objects after successful or failed deliveries.

## Key Types
- **DeliverPayloadData (struct)**: Stores configuration data for payload delivery, such as distances, drop offsets, and weapon settings.
- **DeliverPayloadAIUpdate (class)**: Manages the AI update logic for delivering payloads.
- **DeliverPayloadStateMachine (class)**: Represents the state machine used by `DeliverPayloadAIUpdate`.
- **ConsiderNewApproachState (class)**: A state in the state machine that handles finding a new approach path.
- **RecoverFromOffMapState (class)**: Handles recovery when an object goes off-map.
- **HeadOffMapState (class)**: Manages moving an object off-map.
- **CleanUpState (class)**: Cleans up and destroys objects after delivery.

## Key Functions
### getFieldParse
- Purpose: Provides field parsing for `DeliverPayloadData`.
- Calls: None

### makeStateMachine
- Purpose: Creates a new state machine instance.
- Calls: newInstance(AIStateMachine)

### DeliverPayloadAIUpdate
- Purpose: Constructor for the `DeliverPayloadAIUpdate` class.
- Calls: None

### ~DeliverPayloadAIUpdate
- Purpose: Destructor for the `DeliverPayloadAIUpdate` class.
- Calls: deleteInstance, clear

### getAiFreeToExit
- Purpose: Determines if the AI is free to exit.
- Calls: isEffectivelyDead, getObject

### killDeliveryDecal
- Purpose: Clears the delivery decal.
- Calls: clear

### isAllowedToRespondToAiCommands
- Purpose: Checks if the AI can respond to commands.
- Calls: isAllowedToRespondToAiCommands (base class)

### update
- Purpose: Updates the state machine and handles diving logic.
- Calls: update, getDistanceSquared, setUsePreciseZPos, addAudioEvent, fireCurrentWeapon, doFXPos

### deliverPayload
- Purpose: Initializes payload delivery with specific parameters.
- Calls: deleteInstance, createRadiusDecal, showSubObject, newInstance(DeliverPayloadStateMachine), initDefaultState

### deliverPayloadViaModuleData
- Purpose: Delivers payload using module data.
- Calls: getDeliverPayloadAIUpdateModuleData, deliverPayload

### getPutInContainerTemplateViaModuleData
- Purpose: Retrieves the template for putting items in a container via module data.
- Calls: findTemplate

### calcMinTurnRadius
- Purpose: Calculates the minimum turn radius for an object.
- Calls: getMaxSpeedForCondition, getMaxTurnRate

### isCloseEnoughToTarget
- Purpose: Checks if the object is close enough to its target.
- Calls: getDistanceSquared

### isOffMap
- Purpose: Determines if the object is off-map.
- Calls: getExtentIncludingBorder

## Globals
- None

## Dependencies
- **Includes**: PreRTS.h, Common/Player.h, Common/RandomValue.h, Common/ThingFactory.h, Common/ThingTemplate.h, Common/Xfer.h, GameClient/Drawable.h, GameClient/FXList.h, GameClient/InGameUI.h, GameLogic/Locomotor.h, GameLogic/Module/BodyModule.h, GameLogic/Module/ContainModule.h, GameLogic/Module/D
