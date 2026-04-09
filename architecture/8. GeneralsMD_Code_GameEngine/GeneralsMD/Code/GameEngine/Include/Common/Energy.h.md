# GeneralsMD/Code/GameEngine/Include/Common/Energy.h

## Purpose
Manages player energy production, consumption, and power state in the game.

## Responsibilities
- Tracks energy production/consumption for a player
- Handles power bonuses and sabotage effects
- Manages object influence on energy (entering/leaving)
- Provides energy supply ratio calculations
- Supports serialization via Snapshot interface

## Key Types
- **Energy (Class)**: Encapsulates player energy management
- **Player (Class)**: Owner reference (forward declared)
- **Object (Class)**: Objects affecting energy (forward declared)

## Key Functions
### `init(Player *owner)`
- Purpose: Resets energy values and sets owner
- Calls: None

### `adjustPower(Int powerDelta, Bool adding)`
- Purpose: Modifies energy production/consumption
- Calls: `addProduction`, `addConsumption`

### `objectEnteringInfluence(Object *obj)`
- Purpose: Registers object's energy impact
- Calls: `addPowerBonus`

### `objectLeavingInfluence(Object *obj)`
- Purpose: Removes object's energy impact
- Calls: `removePowerBonus`

### `getEnergySupplyRatio()`
- Purpose: Calculates production-to-consumption ratio
- Calls: None

### `crc(Xfer *xfer)`, `xfer(Xfer *xfer)`, `loadPostProcess()`
- Purpose: Snapshot serialization methods
- Calls: None

## Globals
- None

## Dependencies
- `Common/Snapshot.h` (inheritance)
- `Player`, `Object` (forward declarations)
- `Xfer` (for serialization)
