# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/FiringTracker.cpp

## Purpose
Manages weapon firing state, tracking consecutive shots at targets and handling weapon cooldowns, audio, and continuous fire modes.

## Responsibilities
- Tracks consecutive shots fired at specific targets
- Manages weapon cooldown timers and continuous fire states
- Handles weapon audio events (looping and one-shot sounds)
- Controls weapon reload behavior when idle
- Updates weapon model conditions for visual feedback

## Key Types
- **FiringTracker (Class)**: Manages weapon firing state and tracking
- **UpdateModule (Class)**: Base class for updateable game modules

## Key Functions
### `shotFired`
- Purpose: Records a weapon shot and updates firing state
- Calls: `TheGameLogic->findObjectByID`, `getObject()->testWeaponBonusCondition`, `speedUp`, `coolDown`, `TheAudio->addAudioEvent`, `TheAudio->isCurrentlyPlaying`

### `update`
- Purpose: Handles cooldown timers and audio management
- Calls: `TheAudio->removeAudioEvent`, `getObject()->reloadAllAmmo`, `coolDown`, `calcTimeToSleep`

### `speedUp`
- Purpose: Increases weapon firing rate based on consecutive shots
- Calls: `TheAudio->addAudioEvent`, `getObject()->setWeaponBonusCondition`, `getObject()->clearWeaponBonusCondition`, `getObject()->clearAndSetModelConditionFlags`

### `coolDown`
- Purpose: Resets weapon firing rate and cooldown state
- Calls: `getObject()->clearWeaponBonusCondition`, `getObject()->clearAndSetModelConditionFlags`

### `calcTimeToSleep`
- Purpose: Calculates optimal sleep time based on active timers
- Calls: `TheGameLogic->getFrame`

## Globals
- **TheAudio (GameAudio)**: Handles audio events
- **TheGameLogic (GameLogic)**: Provides game state access

## Dependencies
- `Common/AudioHandleSpecialValues.h`
- `Common/GameType.h`
- `Common/GameAudio.h`
- `Common/PerfTimer.h`
- `Common/ThingTemplate.h`
- `Common/Xfer.h`
- `GameLogic/FiringTracker.h`
- `GameLogic/GameLogic.h`
- `GameLogic/Module/ObjectHelper.h`
- `GameLogic/Object.h`
- `GameLogic/Weapon.h`
