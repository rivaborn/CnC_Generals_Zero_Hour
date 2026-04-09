# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StructureCollapseUpdate.cpp

## Purpose
Handles the animation and effects of structures collapsing after being destroyed.

## Responsibilities
- Manages collapse timing and physics (velocity, height)
- Triggers phase-specific effects (FX, OCL)
- Updates visual representation during collapse
- Handles cleanup after collapse completion

## Key Types
- **StructureCollapseUpdate (class)**: Manages collapse logic
- **StructureCollapseUpdateModuleData (class)**: Contains configuration data
- **StructureCollapsePhaseType (enum)**: Defines collapse phases (INITIAL, DELAY, BURST, FINAL)
- **StructureCollapseStateType (enum)**: Tracks collapse state (STANDING, WAITINGFORCOLLAPSESTART, COLLAPSING, DONE)

## Key Functions
### parseFX
- Purpose: Parses FXList references from INI for specific collapse phases
- Calls: INI::scanIndexList, TheFXListStore->findFXList

### parseOCL
- Purpose: Parses ObjectCreationList references from INI for specific collapse phases
- Calls: INI::scanIndexList, TheObjectCreationListStore->findObjectCreationList

### inList
- Purpose: Checks if a value exists in an integer array
- Calls: None

### buildNonDupRandomIndexList
- Purpose: Generates a list of unique random indices
- Calls: GameLogicRandomValue, inList

### doPhaseStuff
- Purpose: Executes phase-specific effects (FX/OCL) at target position
- Calls: buildNonDupRandomIndexList, FXList::doFXPos, ObjectCreationList::create

### beginStructureCollapse
- Purpose: Initializes collapse sequence with delay
- Calls: doPhaseStuff, GameLogicRandomValue

### update
- Purpose: Updates collapse state and physics each frame
- Calls: doPhaseStuff, GameLogicRandomValue, TheGameLogic->getFrame

## Globals
- **MAX_IDX (const Int)**: Maximum index list size (32)
- **TheStructureCollapsePhaseNames (static const char**)**: String names for collapse phases

## Dependencies
- Common/Thing.h, Common/ThingTemplate.h, Common/INI.h, Common/RandomValue.h
- GameClient/FXList.h, GameLogic/GameLogic.h, GameLogic/Module/StructureCollapseUpdate.h
- GameLogic/ObjectCreationList.h, GameClient/Drawable.h, GameClient/InGameUI.h
