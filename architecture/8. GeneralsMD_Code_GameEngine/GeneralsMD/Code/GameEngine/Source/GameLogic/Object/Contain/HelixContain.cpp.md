# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/HelixContain.cpp

## Purpose
Manages containment logic for Helix units, including portable structures and payload handling.

## Responsibilities
- Handles creation and management of payload objects
- Manages portable structure containment (e.g., Gattling Cannon)
- Synchronizes portable structure position/orientation with container
- Manages damage state propagation to portable structures
- Handles containment state changes (capture, death, etc.)

## Key Types
- **HelixContainModuleData (Class)**: Module data for Helix containment, stores payload template names and drawing flags
- **HelixContain (Class)**: Main containment module for Helix units, extends TransportContain
- **None**: No other significant types defined

## Key Functions
### `createPayload()`
- Purpose: Creates initial payload objects defined in module data
- Calls: `TheThingFactory->findTemplate`, `TheThingFactory->newObject`, `contain->addToContain`

### `update()`
- Purpose: Updates portable structure position/orientation to match container
- Calls: `getPortableStructure()`, `getObject()->getPosition()`, `getObject()->getOrientation()`, `TransportContain::update()`

### `onContaining(Object *obj, Bool wasSelected)`
- Purpose: Handles object containment logic, including weapon bonuses and stealth
- Calls: `TransportContain::onContaining`, `obj->setWeaponBonusCondition`, `obj->setDisabled`, `obj->getStealth()->receiveGrant`

### `onRemoving(Object *obj)`
- Purpose: Handles object removal logic, clearing weapon bonuses and disabled state
- Calls: `TransportContain::onRemoving`, `obj->clearWeaponBonusCondition`, `obj->clearDisabled`

### `xfer(Xfer *xfer)`
- Purpose: Serialization method for network synchronization
- Calls: `TransportContain::xfer`, `xfer->xferVersion`, `xfer->xferObjectID`

## Globals
- **None**: No global/static variables defined

## Dependencies
- Key includes: `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `Common/ThingTemplate.h`, `Common/ThingFactory.h`, `GameClient/ControlBar.h`, `GameClient/Drawable.h`, `GameLogic/Module/BodyModule.h`, `GameLogic/Module/HelixContain.h`, `GameLogic/Object.h`, `GameLogic/PartitionManager.h`, `GameLogic/GameLogic.h`, `GameLogic/Weapon.h`
- External symbols: `TheThingFactory`, `TheGameLogic`, `INVALID_ID`, `KINDOF_PORTABLE_STRUCTURE`, `KINDOF_INFANTRY`, `OBJECT_STATUS_STE
