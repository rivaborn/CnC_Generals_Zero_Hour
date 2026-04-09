# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StructureToppleUpdate.h

## Purpose
Defines the `StructureToppleUpdate` module for handling building collapse animations and damage effects in the game.

## Responsibilities
- Manages building topple animations across multiple phases (initial, delay, final).
- Applies crushing damage to objects in the topple path.
- Handles particle effects and object creation lists tied to topple phases.
- Tracks topple state and progression via update calls.

## Key Types
- **FXBoneInfo (struct)**: Maps bone names to particle system templates.
- **AngleFXInfo (struct)**: Stores angle-based FX lists for topple effects.
- **StructureTopplePhaseType (enum)**: Defines topple phases (INITIAL, DELAY, FINAL).
- **StructureToppleStateType (enum)**: Tracks topple state (STANDING, TOPPLING, DONE, etc.).
- **StructureToppleUpdateModuleData (class)**: Holds module configuration (delays, FX lists, OCLs).
- **StructureToppleUpdate (class)**: Core module implementing topple logic and damage.

## Key Functions
### `beginStructureTopple`
- Purpose: Initiates the topple sequence.
- Calls: `doToppleStartFX`, `doPhaseStuff`

### `applyCrushingDamage`
- Purpose: Applies damage along the topple path.
- Calls: `doDamageLine`

### `doToppleStartFX`
- Purpose: Plays FX at the start of topple.
- Calls: None (FXList playback handled externally).

### `doToppleDelayBurstFX`
- Purpose: Triggers burst FX during delay phase.
- Calls: None

### `doToppleDoneStuff`
- Purpose: Handles cleanup/post-topple effects.
- Calls: None

### `doAngleFX`
- Purpose: Applies angle-specific FX during topple.
- Calls: None

### `doPhaseStuff`
- Purpose: Manages phase-specific logic (OCLs, delays).
- Calls: None

## Globals
- **TheStructureTopplePhaseNames (const char**)**: String names for phase types.

## Dependencies
- `BehaviorModule.h`, `UpdateModule.h`, `DieModule.h`
- `ParticleSys.h`, `RandomValue.h`
- `FXList`, `ObjectCreationList` (forward-declared)
