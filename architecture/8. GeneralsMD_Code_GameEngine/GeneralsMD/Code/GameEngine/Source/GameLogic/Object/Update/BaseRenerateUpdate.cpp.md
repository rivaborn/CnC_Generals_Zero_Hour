# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/BaseRenerateUpdate.cpp

## Purpose
Implements health regeneration logic for base objects in the game.

## Responsibilities
- Manages automatic health regeneration for base objects
- Handles damage events to control regeneration timing
- Implements update logic with configurable regeneration rates
- Manages sleep/wake cycles for performance optimization

## Key Types
- `BaseRegenerateUpdateModuleData` (Class): Module data container
- `BaseRegenerateUpdate` (Class): Main update module for base regeneration

## Key Functions
### `BaseRegenerateUpdate::onDamage`
- Purpose: Adjusts regeneration timing when damage is received
- Calls: `setWakeFrame`

### `BaseRegenerateUpdate::update`
- Purpose: Handles periodic health regeneration
- Calls: `getObject`, `testStatus`, `getBodyModule`, `attemptHealing`

### `BaseRegenerateUpdate::crc`
- Purpose: Handles CRC calculation for network synchronization
- Calls: `UpdateModule::crc`

### `BaseRegenerateUpdate::xfer`
- Purpose: Handles data serialization
- Calls: `UpdateModule::xfer`

## Globals
- `TheGlobalData->m_baseRegenHealthPercentPerSecond` (Real): Controls regeneration rate
- `TheGlobalData->m_baseRegenDelay` (Int): Controls delay after damage

## Dependencies
- `PreRTS.h`, `Common/GlobalData.h`, `GameLogic/GameLogic.h`
- `GameLogic/Module/BaseRegenerateUpdate.h`, `GameLogic/Module/BodyModule.h`
- `GameLogic/Object.h`
