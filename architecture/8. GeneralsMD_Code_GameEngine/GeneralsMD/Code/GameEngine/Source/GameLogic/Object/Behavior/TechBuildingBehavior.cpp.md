# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/TechBuildingBehavior.cpp

## Purpose
Implements behavior for tech buildings in the game, handling capture states and visual effects.

## Responsibilities
- Manages building capture state and visual feedback
- Controls pulse FX rendering when captured
- Handles building death and team reassignment
- Serializes/deserializes module data

## Key Types
- **TechBuildingBehaviorModuleData (struct)**: Stores pulse FX and rate data
- **TechBuildingBehavior (class)**: Main behavior module for tech buildings

## Key Functions
### `update`
- Purpose: Updates building state and pulse FX rendering
- Calls: `FXList::doFXObj`, `setModelConditionState`, `clearModelConditionState`

### `onDie`
- Purpose: Handles building destruction and team reassignment
- Calls: `clearModelConditionState`, `setTeam`

### `onCapture`
- Purpose: Handles building capture events
- Calls: `setWakeFrame`

### `buildFieldParse` (static)
- Purpose: Parses INI data for module configuration
- Calls: `UpdateModuleData::buildFieldParse`

## Globals
- None

## Dependencies
- `PreRTS.H`, `Common/Player.h`, `Common/PlayerList.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `GameClient/FXList.h`, `GameClient/InGameUI.h`, `GameLogic/Module/TechBuildingBehavior.h`, `GameLogic/Object.h`
