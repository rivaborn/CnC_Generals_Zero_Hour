# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/DestroyDie.cpp

## Purpose
Implements the default "Die" module behavior for game objects, handling destruction logic.

## Responsibilities
- Constructs/destructs the DestroyDie module
- Handles object destruction via `onDie` callback
- Manages serialization (Xfer) and CRC for network sync
- Performs post-load initialization

## Key Types
- **DestroyDie (Class)**: Default die module that destroys the associated object when triggered.

## Key Functions
### `DestroyDie::DestroyDie`
- Purpose: Constructor for DestroyDie module.
- Calls: `DieModule` constructor.

### `DestroyDie::onDie`
- Purpose: Callback invoked when the object dies; destroys the object if applicable.
- Calls: `getObject`, `isDieApplicable`, `TheGameLogic->destroyObject`.

### `DestroyDie::crc`
- Purpose: Generates/verifies CRC for network synchronization.
- Calls: `DieModule::crc`.

### `DestroyDie::xfer`
- Purpose: Serializes/deserializes the module state.
- Calls: `DieModule::xfer`.

### `DestroyDie::loadPostProcess`
- Purpose: Performs post-load initialization.
- Calls: `DieModule::loadPostProcess`.

## Globals
- **None**

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/GameLogic.h`, `GameLogic/Module/DestroyDie.h`
- `DieModule`, `Xfer`, `DamageInfo`, `Object`, `TheGameLogic`
