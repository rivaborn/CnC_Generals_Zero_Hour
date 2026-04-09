# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/OverchargeBehavior.cpp

## Purpose
Implements the overcharge behavior for power plants, allowing temporary power boost at the cost of health.

## Responsibilities
- Manages overcharge state (active/inactive)
- Applies health drain during overcharge
- Handles power bonus addition/removal for players
- Manages visual effects (rod extension) via PowerPlantUpdateInterface
- Handles object capture/transfer scenarios

## Key Types
- OverchargeBehaviorModuleData (struct): Stores configuration for health drain rates and minimum health thresholds
- OverchargeBehavior (class): Main behavior module implementing overcharge logic

## Key Functions
### OverchargeBehavior::update
- Purpose: Handles periodic updates including health drain and overcharge termination
- Calls: getObject, getOverchargeBehaviorModuleData, getBodyModule, attemptDamage, enable, TheInGameUI->message, TheRadar->createEvent

### OverchargeBehavior::enable
- Purpose: Activates/deactivates overcharge state and manages associated effects
- Calls: getObject, getBehaviorModules, getPowerPlantUpdateInterface, extendRods, getControllingPlayer, addPowerBonus, removePowerBonus, setWakeFrame

### OverchargeBehavior::onCapture
- Purpose: Handles power bonus transfer when object is captured
- Calls: getObject, isDisabled, getControllingPlayer, removePowerBonus, addPowerBonus

### OverchargeBehavior::loadPostProcess
- Purpose: Restores power bonus after loading
- Calls: getObject, getControllingPlayer, addPowerBonus

## Globals
None

## Dependencies
- Common/Player.h, Common/PlayerList.h, Common/Radar.h, Common/Xfer.h
- GameLogic/GameLogic.h, GameLogic/Object.h
- GameLogic/Module/BodyModule.h, GameLogic/Module/OverchargeBehavior.h, GameLogic/Module/PowerPlantUpdate.h
- GameClient/InGameUI.h
