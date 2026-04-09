# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/HackInternetAIUpdate.cpp

## Purpose
This file implements the AI logic for a unit that can hack into internet systems to gain cash, including state management and command handling.

## Responsibilities
- Manages the state machine for hacking, packing, and unpacking.
- Handles AI commands and ensures they are processed correctly during specific states.
- Updates the unit's state and performs actions like adding money to the player's account.

## Key Types
- HackInternetAIUpdate (Class): Manages the AI logic for internet hacking.
- HackInternetStateMachine (Class): State machine for handling different states of hacking, packing, and unpacking.
- UnpackingState (Class): Represents the state where the unit is unpacking.
- PackingState (Class): Represents the state where the unit is packing.
- HackInternetState (Class): Represents the state where the unit is actively hacking.

## Key Functions
### makeStateMachine
- Purpose: Creates and returns a new instance of the HackInternetStateMachine.
- Calls: newInstance(HackInternetStateMachine)

### HackInternetAIUpdate
- Purpose: Constructor for the HackInternetAIUpdate class.
- Calls: None

### ~HackInternetAIUpdate
- Purpose: Destructor for the HackInternetAIUpdate class.
- Calls: None

### isIdle
- Purpose: Checks if the unit is idle, considering pending commands.
- Calls: AIUpdateInterface::isIdle

### isHacking
- Purpose: Checks if the unit is currently hacking.
- Calls: getStateMachine()->getCurrentStateID

### isHackingPackingOrUnpacking
- Purpose: Checks if the unit is in a hacking, packing, or unpacking state.
- Calls: getStateMachine()->getCurrentStateID

### update
- Purpose: Updates the AI logic, handling pending commands and state transitions.
- Calls: AIUpdateInterface::isIdle, aiDoCommand, AIUpdateInterface::update

### aiDoCommand
- Purpose: Handles AI commands, ensuring they are processed correctly during specific states.
- Calls: isAllowedToRespondToAiCommands, getStateMachine()->getCurrentStateID, getStateMachine()->clear, setLastCommandSource, getStateMachine()->setState

### hackInternet
- Purpose: Initiates the hacking process by setting the state machine to unpacking.
- Calls: getStateMachine()->setState

### crc
- Purpose: Handles CRC operations for serialization.
- Calls: AIUpdateInterface::crc

### xfer
- Purpose: Handles serialization and deserialization of the object.
- Calls: AIUpdateInterface::xfer, m_pendingCommand.doXfer

### loadPostProcess
- Purpose: Performs post-load processing.
- Calls: AIUpdateInterface::loadPostProcess

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Player.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "GameClient/Drawable.h"
  - "GameClient/InGameUI.h"
  - "GameClient/GameText.h"
  - "GameLogic/ExperienceTracker.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/ContainModule.h"
  - "GameLogic/Module/HackInternetAIUpdate.h"
  - "GameLogic/Module/PhysicsUpdate.h"
  - "GameLogic/Object.h"
