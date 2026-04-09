# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/PowerPlantUpgrade.cpp

## Purpose
Handles power plant upgrade logic, including power bonus management and upgrade state persistence.

## Responsibilities
- Manages power plant upgrades and their effects
- Handles power bonus application/removal for players
- Manages upgrade state during object capture and deletion
- Persists upgrade state through save/load

## Key Types
- `PowerPlantUpgrade` (Class): Manages power plant upgrade functionality
- `PowerPlantUpdateInterface` (Interface): Used to extend power rods

## Key Functions
### `onDelete`
- Purpose: Cleans up power bonus when upgrade is deleted
- Calls: `isAlreadyUpgraded()`, `getObject()`, `getControllingPlayer()`, `removePowerBonus()`, `setUpgradeExecuted()`

### `onCapture`
- Purpose: Transfers power bonus during object capture
- Calls: `isAlreadyUpgraded()`, `getObject()`, `isDisabled()`, `getControllingPlayer()`, `removePowerBonus()`, `addPowerBonus()`, `setUpgradeExecuted()`

### `upgradeImplementation`
- Purpose: Applies power plant upgrade effects
- Calls: `getObject()`, `getControllingPlayer()`, `addPowerBonus()`, `getBehaviorModules()`, `extendRods()`

### `loadPostProcess`
- Purpose: Reapplies power bonus after loading
- Calls: `isAlreadyUpgraded()`, `getObject()`, `getControllingPlayer()`, `addPowerBonus()`

## Globals
None

## Dependencies
- `PreRTS.h`, `ModelState.h`, `Player.h`, `Xfer.h`, `Drawable.h`, `InGameUI.h`, `Object.h`, `PowerPlantUpdate.h`, `PowerPlantUpgrade.h`
- `Thing`, `UpgradeModule`, `Player`, `Xfer`, `BehaviorModule`, `PowerPlant
