# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyWarehouseCripplingBehavior.h

## Purpose
Defines behavior for crippling supply warehouses when damaged, including healing mechanics.

## Responsibilities
- Manages damage states and healing for supply warehouses
- Controls building functionality based on damage state
- Handles timing for self-healing suppression
- Manages visual effects for crippled state

## Key Types
- **SupplyWarehouseCripplingBehaviorModuleData (Class)**: Contains healing parameters (suppression time, delay, amount)
- **SupplyWarehouseCripplingBehavior (Class)**: Implements the crippling behavior logic
- **SupplyWarehouseCripplingBehaviorMagicEnum (Enum)**: Not inferable
- **SupplyWarehouseCripplingBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### SupplyWarehouseCripplingBehaviorModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

### SupplyWarehouseCripplingBehavior::onDamage
- Purpose: Handles damage events and suppresses healing
- Calls: resetSelfHealSupression

### SupplyWarehouseCripplingBehavior::onBodyDamageStateChange
- Purpose: Manages state transitions between damaged/crippled states
- Calls: startCrippledEffects, stopCrippledEffects

### SupplyWarehouseCripplingBehavior::update
- Purpose: Handles periodic healing and state updates
- Calls: Not inferable

### SupplyWarehouseCripplingBehavior::resetSelfHealSupression
- Purpose: Resets healing suppression timer after damage
- Calls: Not inferable

### SupplyWarehouseCripplingBehavior::startCrippledEffects
- Purpose: Disables building functionality when crippled
- Calls: Not
