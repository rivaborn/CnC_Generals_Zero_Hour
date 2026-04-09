# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RiderChangeContain.h

## Purpose
Defines the `RiderChangeContain` module for handling transport units that switch riders (e.g., combat bikes).

## Responsibilities
- Manages rider switching logic for transport units
- Handles container validation, capture events, and rider management
- Provides exit door reservation and container UI display

## Key Types
- **WeaponSetType (Enum)**: Not inferable.
- **ObjectStatusType (Enum)**: Not inferable.
- **LocomotorSetType (Enum)**: Not inferable.
- **RiderInfo (Struct)**: Stores rider template data (name, weapon set, status, command set, locomotor type).
- **RiderChangeContainModuleData (Class)**: Module data containing rider configurations and scuttle settings.
- **RiderChangeContain (Class)**: Main container class for rider-switching transports.
- **RiderChangeContainMagicEnum (Enum)**: Not inferable.
- **RiderChangeContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### `RiderChangeContainModuleData::parseRiderInfo`
- Purpose: Parses rider configuration from INI files.
- Calls: Not inferable.

### `RiderChangeContain::isValidContainerFor`
- Purpose: Checks if an object can be contained.
- Calls: Not inferable.

### `RiderChangeContain::onCapture`
- Purpose: Handles rider ejection on capture.
- Calls: Not inferable.

### `RiderChangeContain::update`
- Purpose: Frame update logic for rider management.
- Calls: Not inferable.

### `RiderChangeContain::reserveDoorForExit`
- Purpose: Reserves an exit door for a rider.
- Calls: Not inferable.

## Globals
- **
