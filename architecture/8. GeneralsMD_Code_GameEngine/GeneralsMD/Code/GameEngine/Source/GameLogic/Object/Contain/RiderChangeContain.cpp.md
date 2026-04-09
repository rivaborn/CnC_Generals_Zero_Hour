# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/RiderChangeContain.cpp

## Purpose
Handles the "combat bike" transport system where units can switch places, including model condition changes and experience transfer.

## Responsibilities
- Manages rider-specific model conditions, weapon sets, and status flags
- Handles experience transfer between rider and bike
- Controls bike scuttling after rider dismounts
- Validates which units can board the bike

## Key Types
- **RiderChangeContainModuleData (Class)**: Stores rider templates, model conditions, weapon sets, and scuttling parameters
- **RiderInfo (Struct)**: Contains template name, model condition flags, weapon set flags, object status, command set, and locomotor set type
- **RiderChangeContain (Class)**: Implements the rider change containment logic

## Key Functions
### `isValidContainerFor`
- Purpose: Checks if a unit can board the bike and has space
- Calls: `TransportContain::isValidContainerFor`, `TheThingFactory->findTemplate`

### `onContaining`
- Purpose: Handles unit boarding the bike, including model condition changes and experience transfer
- Calls: `getAI()->aiEvacuateInstantly`, `setModelConditionState`, `setWeaponSetFlag`, `setStatus`, `setCommandSetStringOverride`, `chooseLocomotorSet`, `markAsDetected`, `setVeterancyLevel`

### `onRemoving`
- Purpose: Handles unit dismounting, including scuttling the bike
- Calls: `TheGameLogic->destroyObject`, `TransportContain::onRemoving`, `clearModelConditionFlags`, `clearWeaponSetFlag`, `clearStatus`, `setVeterancyLevel`, `setStatus`, `setModelConditionState`, `isMoving`

### `update`
- Purpose: Handles bike scuttling timer and destruction
- Calls: `TheGameLogic->getFrame`, `getObject()->kill`

## Globals
- **MAX_RIDERS (const int)**: Maximum number of rider types (8)

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/ThingTemplate.h`, `GameLogic/AI.h`, `GameLogic/Module/RiderChangeContain.h`
- `TransportContain` (base class)
- `TheThingFactory`, `TheMessageStream`, `TheInGameUI`, `TheControlBar`, `ThePlayerList`, `TheGameLogic`
