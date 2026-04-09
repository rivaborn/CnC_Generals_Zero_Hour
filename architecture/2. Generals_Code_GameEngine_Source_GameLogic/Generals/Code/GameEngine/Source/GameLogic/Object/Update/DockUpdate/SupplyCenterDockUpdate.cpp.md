# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/SupplyCenterDockUpdate.cpp

## Purpose
This file implements the logic for a supply center dock update, which processes supply trucks docking to convert boxes into money for the owning player.

## Responsibilities
- Handle the action of supply trucks docking at a supply center.
- Update the player's money and score based on the value of the boxes.
- Display floating text indicating the amount of money earned.

## Key Types
- `SupplyCenterDockUpdateModuleData (struct)`: Data structure for supply center dock update module.
- `SupplyCenterDockUpdate (class)`: Class handling the logic for supply center dock updates.

## Key Functions
### SupplyCenterDockUpdate::action
- Purpose: Processes the docking action of a supply truck, converting boxes into money and updating player stats.
- Calls:
  - `getAIUpdateInterface()`
  - `getSupplyTruckAIInterface()`
  - `loseOneBox()`
  - `getSupplyBoxValue()`
  - `deposit()`
  - `addMoneyEarned()`
  - `fetch()`
  - `getGroundHeight()`
  - `addFloatingText()`

### SupplyCenterDockUpdate::update
- Purpose: Updates the supply center dock state.
- Calls:
  - `update()` (base class)
  - `findCreateModule()`
  - `shouldDoOnBuildComplete()`

## Globals
None

## Dependencies
- Includes:
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/SupplyCenterDockUpdate.h"
  - "GameLogic/Module/SupplyTruckAIUpdate.h"
  - "GameClient/Color.h"
  - "GameClient/InGameUI.h"
  - "GameClient/GameText.h"
