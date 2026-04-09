# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StructureToppleUpdate.cpp

## Purpose
Handles the animation and effects of buildings toppling over when destroyed.

## Responsibilities
- Manages the topple animation sequence (delay, topple, crushing, done states)
- Spawns visual/audio effects during topple phases
- Applies crushing damage to terrain/units beneath the falling building
- Handles object creation lists for debris/particles at different topple phases

## Key Types
- **StructureToppleUpdate (Class)**: Manages building topple behavior
- **StructureToppleUpdateModuleData (Class)**: Contains configuration data for topple effects
- **AngleFXInfo (Struct)**: Stores angle-based effect triggers
- **StructureTopplePhaseType (Enum)**: Defines topple phases (initial, delay, final)
- **StructureToppleStateType (Enum)**: Tracks current topple state (standing, waiting, toppling, done)

## Key Functions
### beginStructureTopple
- Purpose: Initiates the topple sequence after building destruction
- Calls: doToppleStartFX, TheScriptEngine->adjustToppleDirection

### update
- Purpose: Handles state transitions and animations during topple
- Calls: doToppleDelayBurstFX, doAngleFX, applyCrushingDamage, doPhaseStuff

### applyCrushingDamage
- Purpose: Applies damage along the building's topple path
- Calls: doDamageLine, TheWeaponStore->createAndFireTempWeapon

### doPhaseStuff
- Purpose: Spawns phase-specific object creation lists
- Calls: ObjectCreationList::create, buildNonDupRandomIndexList

## Globals
- **MAX_IDX (const Int)**: Maximum index list size (32)

## Dependencies
- Common/Thing.h, Common/INI.h, GameClient/FXList.h
- GameLogic/GameLogic.h, GameLogic/Module/StructureToppleUpdate.h
- GameLogic/Object.h, GameLogic/Weapon.h
- GameClient/Drawable.h, GameClient/InGameUI.h
