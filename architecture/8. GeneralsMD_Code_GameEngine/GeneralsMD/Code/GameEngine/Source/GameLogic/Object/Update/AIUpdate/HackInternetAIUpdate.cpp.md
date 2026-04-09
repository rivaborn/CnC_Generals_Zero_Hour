# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/HackInternetAIUpdate.cpp

## Purpose
Handles the AI logic for internet hacking units, managing state transitions for packing, unpacking, and cash generation.

## Responsibilities
- Manages state machine for hacking operations (packing/unpacking/hacking)
- Controls cash generation based on unit veterancy
- Handles AI command queuing during hacking operations
- Manages unit model conditions and animations
- Processes audio and visual feedback for hacking

## Key Types
- **HackInternetAIUpdate (Class)**: Main AI update interface for hacking units
- **HackInternetStateMachine (Class)**: State machine managing hacking operations
- **UnpackingState (Class)**: State handling unit unpacking animation
- **PackingState (Class)**: State handling unit packing animation
- **HackInternetState (Class)**: State handling actual cash generation

## Key Functions
### `aiDoCommand`
- Purpose: Processes AI commands with special handling for hacking operations
- Calls: `isAllowedToRespondToAiCommands`, `AIUpdateInterface::aiDoCommand`

### `hackInternet`
- Purpose: Initiates the hacking process by transitioning to unpacking state
- Calls: `getStateMachine()->setState`

### `update`
- Purpose: Main update loop that processes pending commands and state transitions
- Calls: `AIUpdateInterface::isIdle`, `AIUpdateInterface::update`, `aiDoCommand`

### `HackInternetState::update`
- Purpose: Handles cash generation and veterancy-based rewards
- Calls: `getControllingPlayer()->getMoney()->deposit`, `getExperienceTracker()->addExperiencePoints`

## Globals
- None

## Dependencies
- `AIUpdateInterface`, `AIStateMachine`, `Object`, `Player`, `Money`, `ExperienceTracker`
- `TheAudio`, `TheInGameUI`, `TheGameText`
- `ModuleData` for hacking parameters
- Various game engine utilities for random values and timing
