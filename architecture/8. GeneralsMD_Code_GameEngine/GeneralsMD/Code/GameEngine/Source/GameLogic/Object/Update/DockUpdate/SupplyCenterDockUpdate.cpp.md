# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/SupplyCenterDockUpdate.cpp

## Purpose
Handles the logic for supply centers converting supply boxes into money when docked by supply trucks.

## Responsibilities
- Processes supply box conversion to money
- Handles temporary stealth grants
- Displays floating money text
- Manages supply truck AI interactions

## Key Types
- **SupplyCenterDockUpdateModuleData (Class)**: Stores module-specific data (e.g., stealth grant duration)
- **SupplyCenterDockUpdate (Class)**: Main update class handling docking logic

## Key Functions
### `action(Object* docker, Object *drone)`
- Purpose: Processes docking action, converts supply boxes to money, and handles stealth grants.
- Calls: `getSupplyCenterDockUpdateModuleData()`, `loseOneBox()`, `getUpgradedSupplyBoost()`, `deposit()`, `addMoneyEarned()`, `receiveGrant()`, `addFloatingText()`

### `update()`
- Purpose: Extends base update logic with debug checks.
- Calls: `DockUpdate::update()`

### `crc(Xfer *xfer)`
- Purpose: Handles CRC serialization.
- Calls: `DockUpdate::crc()`

### `xfer(Xfer *xfer)`
- Purpose: Handles Xfer serialization.
- Calls: `DockUpdate::xfer()`

### `loadPostProcess()`
- Purpose: Post-load processing.
- Calls: `DockUpdate::loadPostProcess()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/Module/SupplyCenterDockUpdate.h`, `GameLogic/Module/SupplyTruckAIUpdate.h`, `GameClient/Color.h`, `GameClient/InGameUI.h`, `GameClient/GameText.h`
