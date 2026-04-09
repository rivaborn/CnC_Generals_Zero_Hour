# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/CreateCrateDie.cpp

## Purpose
Handles the creation of crates when an object dies, based on configurable conditions.

## Responsibilities
- Checks conditions for crate creation (chance, veterancy, killer type/science)
- Spawns crates at valid positions around the dead object
- Notifies AI about created crates if killer is computer-controlled
- Manages crate ownership and visual properties

## Key Types
- **CreateCrateDie (Class)**: Die module that creates crates on object death
- **CreateCrateDieModuleData (Class)**: Module data containing crate name list
- **CrateTemplate (Struct)**: Template for crate properties and conditions

## Key Functions
### `onDie`
- Purpose: Handles crate creation when object dies
- Calls: `isDieApplicable`, `testCreationChance`, `testVeterancyLevel`, `testKillerType`, `testKillerScience`, `createCrate`

### `testCreationChance`
- Purpose: Checks if crate creation should happen based on chance
- Calls: `GameLogicRandomValueReal`

### `testKillerType`
- Purpose: Verifies if killer matches required type
- Calls: `getTemplate()->isKindOfMulti`

### `createCrate`
- Purpose: Creates and positions a crate object
- Calls: `ThePartitionManager->findPositionAround`, `TheThingFactory->newObject`

## Globals
- **TheCrateSystem (CrateSystem)**: Access to crate templates
- **TheGameLogic (GameLogic)**: Game state and object lookup
- **TheThingFactory (ThingFactory)**: Object creation
- **ThePartitionManager (PartitionManager)**: Position finding

## Dependencies
- Common: `PlayerList`, `Player`, `RandomValue`, `ThingFactory`, `ThingTemplate`, `Xfer`
- GameLogic: `CrateSystem`, `ExperienceTracker`, `GameLogic`, `Object`, `PartitionManager`
- Modules: `CreateCrateDie.h`, `AIUpdate.h`
