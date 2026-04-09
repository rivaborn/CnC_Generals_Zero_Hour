# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpecialPowerModule.cpp

## Purpose
This file implements the `SpecialPowerModule` class, which manages special powers for game objects in Command & Conquer Generals. It handles initialization, activation, and recharge of special powers.

## Responsibilities
- Manage special power data and state.
- Handle special power activation and recharge logic.
- Update UI elements related to special powers.
- Play audio events associated with special powers.

## Key Types
- `SpecialPowerModuleData` (struct): Stores configuration data for special powers.
- `SpecialPowerModule` (class): Manages the behavior of special powers for game objects.

## Key Functions
### SpecialPowerModule::SpecialPowerModule
- Purpose: Initializes a new instance of `SpecialPowerModule`.
- Calls:
  - `startPowerRecharge`
  - `pauseCountdown`
  - `resolveSpecialPower`

### SpecialPowerModule::~SpecialPowerModule
- Purpose: Cleans up resources when the module is destroyed.
- Calls:
  - `TheInGameUI->removeSuperweapon`

### SpecialPowerModule::onSpecialPowerCreation
- Purpose: Handles the creation of a special power.
- Calls:
  - `startPowerRecharge`
  - `pauseCountdown`
  - `TheInGameUI->addSuperweapon`

### SpecialPowerModule::isReady
- Purpose: Checks if a special power is ready to use.
- Calls:
  - `player->getOrStartSpecialPowerReadyFrame`

### SpecialPowerModule::startPowerRecharge
- Purpose: Starts the recharge process for a special power.
- Calls:
  - `player->resetOrStartSpecialPowerReadyFrame`
  - `TheGameLogic->getFrame`

### SpecialPowerModule::doSpecialPower
- Purpose: Initiates the execution of a special power.
- Calls:
  - `initiateIntentToDoSpecialPower`
  - `triggerSpecialPower`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/GameAudio.h"
  - "Common/GlobalData.h"
  - "Common/INI.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/Science.h"
  - "Common/SpecialPower.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/DeletionUpdate.h"
  - "GameLogic/Module/UpdateModule.h"
  - "GameLogic/Module/SpecialPowerModule.h"
  - "GameLogic/ScriptEngine.h"
  - "GameClient/Eva.h"
  - "GameClient/InGameUI.h"
  - "GameClient/ControlBar.h"

- External symbols:
  - `TheGameLogic`
  - `TheGlobalData`
  - `TheAudio`
  - `TheEva`
  - `TheScriptEngine`
  - `TheThingFactory`
  - `ThePlayerList`
  - `TheInGameUI`
