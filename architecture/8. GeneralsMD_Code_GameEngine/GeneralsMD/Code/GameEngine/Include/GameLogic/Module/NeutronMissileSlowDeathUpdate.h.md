# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/NeutronMissileSlowDeathUpdate.h

## Purpose
Defines the behavior module for the neutron missile superweapon's slow death animation and effects.

## Responsibilities
- Manages timed blast effects after missile impact
- Handles scorch mark placement
- Controls damage application via multiple blast phases
- Tracks completion status of each blast phase

## Key Types
- **NeutronBlast (Enum)**: Identifies individual blast phases (1-9)
- **BlastInfo (Struct)**: Contains parameters for each blast (radius, damage, timing)
- **NeutronMissileSlowDeathBehaviorModuleData (Class)**: Holds configuration data for the behavior
- **NeutronMissileSlowDeathBehavior (Class)**: Implements the timed blast behavior

## Key Functions
### NeutronMissileSlowDeathBehavior::update
- Purpose: Updates blast state and triggers blasts at scheduled times
- Calls: doBlast, doScorchBlast

### NeutronMissileSlowDeathBehavior::doBlast
- Purpose: Applies damage and effects for a specific blast phase
- Calls: Not inferable

### NeutronMissileSlowDeathBehavior::doScorchBlast
- Purpose: Places scorch mark effects for a blast phase
- Calls: Not inferable

## Globals
- None

## Dependencies
- `SlowDeathBehavior.h` (base class)
- `FXList` (forward declaration)
- `MultiIniFieldParse` (for configuration parsing)
