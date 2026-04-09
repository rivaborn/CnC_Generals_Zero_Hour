# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/SupplyWarehouseCripplingBehavior.cpp

## Purpose
This file implements the behavior for a supply warehouse that becomes crippled when damaged and manages its healing process.

## Responsibilities
- Handles damage events to suppress healing.
- Starts and stops crippling effects based on damage state.
- Manages a timer to heal the building periodically after suppression ends.

## Key Types
- `SupplyWarehouseCripplingBehaviorModuleData`: Stores configuration for self-healing behavior.
- `SupplyWarehouseCripplingBehavior`: Implements the logic for supply warehouse crippling behavior.

## Key Functions
### SupplyWarehouseCripplingBehavior::onDamage
- Purpose: Resets healing suppression when the building is damaged.
- Calls: `resetSelfHealSupression`, `setWakeFrame`

### SupplyWarehouseCripplingBehavior::onBodyDamageStateChange
- Purpose: Starts or stops crippling effects based on damage state changes.
- Calls: `startCrippledEffects`, `stopCrippledEffects`

### SupplyWarehouseCripplingBehavior::update
- Purpose: Manages the healing process and updates the next healing frame.
- Calls: `attemptHealing`, `setWakeFrame`

### SupplyWarehouseCripplingBehavior::resetSelfHealSupression
- Purpose: Resets the suppression timer for healing.
- Calls: None

### SupplyWarehouseCripplingBehavior::startCrippledEffects
- Purpose: Starts crippling effects on the building.
- Calls: `setDockCrippled(TRUE)`

### SupplyWarehouseCripplingBehavior::stopCrippledEffects
- Purpose: Stops crippling effects on the building.
- Calls: `setDockCrippled(FALSE)`

## Globals
- None

## Dependencies
- Includes: "PreRTS.h", "Common/Xfer.h", "GameLogic/Module/SupplyWarehouseCripplingBehavior.h", "GameLogic/GameLogic.h", "GameLogic/Object.h", "GameLogic/Module/BodyModule
