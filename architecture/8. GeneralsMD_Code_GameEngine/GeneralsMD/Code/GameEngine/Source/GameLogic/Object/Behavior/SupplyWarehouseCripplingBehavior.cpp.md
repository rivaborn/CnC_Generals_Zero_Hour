# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/SupplyWarehouseCripplingBehavior.cpp

## Purpose
Manages supply warehouse damage states, healing, and docking behavior when damaged.

## Responsibilities
- Handles damage state transitions (e.g., really damaged)
- Manages self-healing with suppression delays
- Controls docking behavior when crippled
- Updates healing state periodically

## Key Types
- `SupplyWarehouseCripplingBehaviorModuleData` (Struct): Stores healing parameters (suppression time, delay, amount)
- `SupplyWarehouseCripplingBehavior` (Class): Behavior module for supply warehouses

## Key Functions
### `onDamage`
- Purpose: Reacts to damage by resetting healing suppression.
- Calls: `resetSelfHealSupression`, `setWakeFrame`

### `onBodyDamageStateChange`
- Purpose: Handles state changes (e.g., really damaged).
- Calls: `startCrippledEffects`, `stopCrippledEffects`

### `update`
- Purpose: Manages periodic healing and sleep timing.
- Calls: `attemptHealing`, `getFrame`

### `resetSelfHealSupression`
- Purpose: Sets healing suppression timer.
- Calls: `getFrame`

### `startCrippledEffects`
- Purpose: Disables docking when really damaged.
- Calls: `setDockCrippled`

### `stopCrippledEffects`
- Purpose: Re-enables docking when healed.
- Calls: `setDockCrippled`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Module/SupplyWarehouseCripplingBehavior.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Module/BodyModule.h`
- `TheGameLogic
