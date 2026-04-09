# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/InstantDeathBehavior.cpp

## Purpose
Implements the InstantDeathBehavior module, which handles object destruction with effects, object creation lists, and weapons.

## Responsibilities
- Parses FX, OCL, and Weapon data from INI files
- Manages death behavior including AI state updates
- Triggers visual/audio effects, spawns objects, and fires weapons on death
- Handles serialization (Xfer) and CRC for network sync

## Key Types
- **InstantDeathBehaviorModuleData (Class)**: Stores FX lists, OCLs, and weapons for death behavior
- **InstantDeathBehavior (Class)**: Implements death behavior logic

## Key Functions
### parseFX
- Purpose: Parses FX list tokens from INI into module data
- Calls: `TheFXListStore->findFXList()`

### parseOCL
- Purpose: Parses OCL tokens from INI into module data
- Calls: `TheObjectCreationListStore->findObjectCreationList()`

### parseWeapon
- Purpose: Parses weapon template tokens from INI into module data
- Calls: `TheWeaponStore->findWeaponTemplate()`

### onDie
- Purpose: Handles death logic including effects, spawns, and weapon fire
- Calls: `FXList::doFXObj()`, `ObjectCreationList::create()`, `TheWeaponStore->createAndFireTempWeapon()`, `TheGameLogic->destroyObject()`

### buildFieldParse
- Purpose: Registers INI field parsers for module data
- Calls: `DieModuleData::buildFieldParse()`

## Globals
- None

## Dependencies
- Common/Thing.h, Common/ThingTemplate.h, Common/INI.h, Common/RandomValue.h, Common/GameLOD.h, Common/Xfer.h
- GameClient/Drawable.h, GameClient/FXList.h, GameClient/InGameUI.h
- GameLogic/GameLogic.h, GameLogic/Module/BodyModule.h, GameLogic/Module/InstantDeathBehavior.h, GameLogic/Module/AIUpdate.h, GameLogic/Object.h, GameLogic/ObjectCreationList.h, GameLogic/Weapon.h
