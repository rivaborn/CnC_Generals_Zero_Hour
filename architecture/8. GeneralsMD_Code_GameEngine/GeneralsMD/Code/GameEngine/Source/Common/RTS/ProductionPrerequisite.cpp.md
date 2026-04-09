# GeneralsMD/Code/GameEngine/Source/Common/RTS/ProductionPrerequisite.cpp

## Purpose
Manages production prerequisites for units in the game, including unit and science requirements.

## Responsibilities
- Tracks unit and science prerequisites for production
- Resolves prerequisite names to templates
- Checks if prerequisites are satisfied for a player
- Generates lists of unsatisfied prerequisites

## Key Types
- **ProductionPrerequisite (Class)**: Manages production prerequisites
- **PrereqUnitRec (Struct)**: Stores unit prerequisite info (name, flags, template)
- **MAX_PREREQ (const Int)**: Maximum number of prerequisites (10)

## Key Functions
### `resolveNames`
- Purpose: Converts prerequisite names to ThingTemplate pointers
- Calls: `TheThingFactory->findTemplate`

### `isSatisfied`
- Purpose: Checks if all prerequisites are met for a player
- Calls: `player->hasScience`, `calcNumPrereqUnitsOwned`

### `getRequiresList`
- Purpose: Generates a list of unsatisfied prerequisites
- Calls: `TheGameText->fetch`

### `addUnitPrereq`
- Purpose: Adds a unit prerequisite (with optional OR logic)
- Calls: None (internal)

## Globals
- **TheThingFactory (ThingFactory*)**: Global factory for finding templates
- **TheGameText (GameText*)**: Global text resource manager

## Dependencies
- `Common/ProductionPrerequisite.h`
- `Common/Player.h`
- `Common/ThingFactory.h`
- `Common/ThingTemplate.h`
- `GameLogic/Object.h`
- `GameClient/Drawable.h`
- `GameClient/GameText.h`
