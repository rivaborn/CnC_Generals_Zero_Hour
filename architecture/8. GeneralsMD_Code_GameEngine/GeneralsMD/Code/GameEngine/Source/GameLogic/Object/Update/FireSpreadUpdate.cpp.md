# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FireSpreadUpdate.cpp

## Purpose
Handles fire spread logic between objects in the game world.

## Responsibilities
- Manages fire propagation from burning objects to nearby flammable objects
- Controls timing of fire spread attempts using random delays
- Creates ember effects when fire spreads
- Filters objects to find only those that can be ignited

## Key Types
- **PartitionFilterFlammable (Class)**: Filters objects to find those that are flammable and can currently be ignited
- **FireSpreadUpdateModuleData (Class)**: Contains configuration data for fire spread behavior
- **FireSpreadUpdate (Class)**: Main update module that handles fire spreading logic

## Key Functions
### PartitionFilterFlammable::allow
- Purpose: Determines if an object should be considered for fire spreading
- Calls: `objOther->findUpdateModule()`

### FireSpreadUpdate::update
- Purpose: Main update loop that handles fire spreading logic
- Calls: `ThePartitionManager->getClosestObject()`, `ObjectCreationList::create()`, `fu->tryToIgnite()`

### FireSpreadUpdate::startFireSpreading
- Purpose: Starts the fire spreading process for an object
- Calls: `setWakeFrame()`

### FireSpreadUpdate::calcNextSpreadDelay
- Purpose: Calculates the random delay until next fire spread attempt
- Calls: `GameLogicRandomValue()`

## Globals
- None

## Dependencies
- `PartitionManager.h` for spatial queries
- `ObjectCreationList.h` for creating ember effects
- `FlammableUpdate.h` for checking object flammability
- `RandomValue.h` for random delay calculation
- `Xfer.h` for serialization support
