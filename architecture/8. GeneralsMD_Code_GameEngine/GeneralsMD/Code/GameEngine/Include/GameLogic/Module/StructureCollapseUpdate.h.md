# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StructureCollapseUpdate.h

## Purpose
Defines the `StructureCollapseUpdate` module for handling building collapse animations and effects in the game.

## Responsibilities
- Manages building collapse state transitions (standing â collapsing â done)
- Handles damage application during collapse
- Controls timing and effects for collapse phases (initial, delay, burst, final)
- Triggers visual and audio effects for collapse events
- Implements memory pooling for performance

## Key Types
- `StructureCollapsePhaseType` (Enum): Defines collapse phases (initial, delay, burst, final)
- `StructureCollapseUpdateModuleData` (Class): Contains configuration data for collapse behavior
- `StructureCollapseUpdate` (Class): Main module class handling collapse logic
- `StructureCollapseStateType` (Enum): Tracks collapse state (standing, waiting, collapsing, done)

## Key Functions
### `update()`
- Purpose: Updates collapse state and triggers phase-specific effects
- Calls: `doPhaseStuff`, `doCollapseDelayBurstFX`, `doCollapseDoneStuff`

### `onDie()`
- Purpose: Initiates collapse sequence when building is destroyed
- Calls: `beginStructureCollapse`

### `doPhaseStuff()`
- Purpose: Executes phase-specific collapse logic (FX, damage, etc.)
- Calls: Not inferable (implementation in .cpp)

### `applyCrushingDamage()`
- Purpose: Applies damage in a directional pattern during collapse
- Calls: `doDamageLine`

## Globals
- None

## Dependencies
- `BehaviorModule.h`, `DieModule.h`, `UpdateModule.h`
- `FXList`, `ObjectCreationList` (forward declarations)
- `MultiIniFieldParse`, `Thing`, `Object`, `WeaponTemplate`, `DamageInfo`, `Coord3D
