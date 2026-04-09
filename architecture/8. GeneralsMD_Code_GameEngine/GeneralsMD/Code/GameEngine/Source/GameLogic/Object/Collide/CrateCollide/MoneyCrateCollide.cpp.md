# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/MoneyCrateCollide.cpp

## Purpose
Handles collision behavior for money crates in the game, granting money to the colliding player.

## Responsibilities
- Grants money to the player who collides with the crate
- Applies upgrade-based supply boosts
- Plays sound effects on crate pickup
- Serializes/deserializes crate data

## Key Types
- **MoneyCrateCollide (Class)**: Manages money crate collision logic
- **upgradePair (Struct)**: Stores upgrade type and boost amount (Not inferable)

## Key Functions
### `executeCrateBehavior`
- Purpose: Grants money to the colliding player and plays sound
- Calls: `getMoneyCrateCollideModuleData`, `getUpgradedSupplyBoost`, `deposit`, `addMoneyEarned`, `setObjectID`, `addAudioEvent`

### `getUpgradedSupplyBoost`
- Purpose: Calculates bonus money from player upgrades
- Calls: `getMoneyCrateCollideModuleData`, `findUpgrade`, `hasUpgradeComplete`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `CrateCollide::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- **TheAudio (AudioSystem)**: Global audio system
- **TheUpgradeCenter (UpgradeCenter)**: Global upgrade manager

## Dependencies
- `PreRTS.h`, `AudioEventRTS.h`, `MiscAudio.h`, `Player.h`, `Xfer.h`, `Object.h`, `MoneyC
