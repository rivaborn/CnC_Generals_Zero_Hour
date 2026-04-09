# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/OverchargeBehavior.cpp

## Purpose
This file implements the `OverchargeBehavior` class, which manages the overcharge state of game objects. During this state, objects produce more power but lose health over time.

## Responsibilities
- Manage the overcharge state of game objects.
- Adjust object health during the overcharge period.
- Handle UI notifications and radar events when overcharge is exhausted.
- Enable or disable the overcharge state based on conditions.

## Key Types
- `OverchargeBehaviorModuleData (struct)`: Stores configuration data for overcharge behavior, such as health drain rate and minimum allowed health percentage.
- `OverchargeBehavior (class)`: Implements the logic for managing the overcharge state of game objects.

## Key Functions
### OverchargeBehavior::update
- Purpose: Updates the object's health during the overcharge state and checks if the overcharge should be disabled.
- Calls:
  - `attemptDamage`
  - `getMaxHealth`
  - `getHealth`

### OverchargeBehavior::toggle
- Purpose: Toggles the overcharge state of the object.
- Calls:
  - `enable`

### OverchargeBehavior::enable
- Purpose: Enables or disables the overcharge state, adjusting power plant rods and player power bonuses accordingly.
- Calls:
  - `extendRods`
  - `addPowerBonus`
  - `removePowerBonus`
  - `setWakeFrame`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/Radar.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/OverchargeBehavior.h"
  - "GameLogic/Module/PowerPlantUpdate.h"
  - "GameClient/InGameUI.h"
