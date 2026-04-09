# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/SlowDeathBehavior.cpp

## Purpose
Implements slow death behavior for game objects, controlling destruction animations, effects, and timing.

## Responsibilities
- Manages timed destruction phases (sinking, midpoint, final)
- Handles flinging objects with physics forces
- Triggers FX, OCLs, and weapons during death phases
- Adjusts death timing based on game LOD settings
- Parses INI configuration for death behavior parameters

## Key Types
- `SlowDeathBehaviorModuleData` (Class): Stores configuration for slow death behavior (sink rates, delays, effects, etc.)
- `SlowDeathBehavior` (Class): Implements the slow death behavior module
- `SlowDeathPhaseType` (Enum): Defines death phases (initial, midpoint, final)

## Key Functions
### `parseFX`
- Purpose: Parses FX lists from INI for specific death phases
- Calls: `TheFXListStore->findFXList`

### `parseOCL`
- Purpose: Parses Object Creation Lists from INI for specific death phases
- Calls: `TheObjectCreationListStore->findObjectCreationList`

### `parseWeapon`
- Purpose: Parses weapon templates from INI for specific death phases
- Calls: `TheWeaponStore->findWeaponTemplate`

### `calcRandomForce`
- Purpose: Calculates random force vector for flinging objects
- Calls: `GameLogicRandomValueReal`

### `beginSlowDeath`
- Purpose: Initiates slow death sequence based on damage info
- Calls: `doPhaseStuff`, `setWakeFrame`, `TheGameLogic->destroyObject`

### `doPhaseStuff`
- Purpose: Executes effects for a specific death phase
- Calls: `FXList::doFXObj`, `ObjectCreationList::create`, `TheWeaponStore->createAndFireTempWeapon`

### `update`
- Purpose: Updates slow death state each frame
- Calls: `TheGameLogic->destroyObject`, `TheGameLogic->findObjectByID`

### `onDie`
- Purpose: Handles death event and selects appropriate death behavior
- Calls: `getProbabilityModifier`, `beginSlowDeath`, `TheGameLogic->deselectObject`

## Globals
- `BEGIN_MIDPOINT_RATIO` (Real): Minimum ratio for midpoint frame calculation
- `END_MIDPOINT_RATIO` (Real): Maximum ratio for midpoint frame calculation

## Dependencies
- `PreRTS.h`, `Common/GameLOD.h`, `Common/INI.h`, `Common/RandomValue.h`, `Common/Thing.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `GameClient/Drawable.h`, `GameClient/FXList.h`, `GameClient/InGameUI.h`
- `GameLogic/GameLogic.h`, `GameLogic/Module/BodyModule.h`, `GameLogic/Module/PhysicsUpdate.h`, `GameLogic/Module/SlowDeathBehavior.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/SlavedUpdate.h`, `GameLogic/Object.h`, `GameLogic/ObjectCreationList.h`, `GameLogic/Weapon.h`
- `TheGameLODManager`, `TheGameLogic`, `TheFXListStore`, `TheObjectCreationListStore`, `TheWeaponStore`, `TheSlowDeathPhaseNames`
