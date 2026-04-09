# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/TransportContain.cpp

## Purpose
Handles transport unit containment logic, including loading/unloading, slot management, and special behaviors like health regeneration and weapon upgrades.

## Responsibilities
- Manages transport slot capacity and occupancy
- Handles loading/unloading of units with special behaviors (position, velocity, orientation)
- Implements health regeneration for transported units
- Manages weapon upgrades based on transported units
- Handles special cases like Jarmen Kell sniper timer transfer

## Key Types
- **TransportContainModuleData (Class)**: Stores transport-specific configuration (slots, exit behaviors, etc.)
- **TransportContain (Class)**: Implements transport containment logic
- **InitialPayload (Struct)**: Stores template name and count for initial payload

## Key Functions
### `isValidContainerFor`
- Purpose: Checks if a unit can be transported and if there's capacity
- Calls: `OpenContain::isValidContainerFor`, `getTransportSlotCount`, `getControllingPlayer`

### `onContaining`
- Purpose: Handles unit loading into transport
- Calls: `OpenContain::onContaining`, `setDisabled`, `setModelConditionState`, `letRidersUpgradeWeaponSet`

### `onRemoving`
- Purpose: Handles unit unloading from transport
- Calls: `OpenContain::onRemoving`, `clearDisabled`, `setPosition`, `setOrientation`, `applyMotiveForce`, `setPitchRate`, `clearModelConditionState`, `setAllowToFall`, `setAttitude`, `wakeUpAndAttemptToTarget`

### `update`
- Purpose: Updates transport state and regenerates health of contained units
- Calls: `createPayload`, `getContainedItemsList`, `attemptHealing`, `OpenContain::update`

### `isSpecificRiderFreeToExit`
- Purpose: Determines if a specific unit can legally exit the transport
- Calls: `getAiFreeToExit`, `isUsingAirborneLocomotor`, `validMovementTerrain`

## Globals
- None

## Dependencies
- Key includes: `PreRTS.h`, `Common/Player.h`, `GameLogic/Module/TransportContain.h`, `GameLogic/Object.h`
- External symbols: `TheGameLogic`, `TheThingFactory`, `TheAI`
