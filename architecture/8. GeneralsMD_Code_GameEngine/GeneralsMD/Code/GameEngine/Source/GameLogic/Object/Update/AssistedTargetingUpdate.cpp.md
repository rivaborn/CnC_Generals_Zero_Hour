# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AssistedTargetingUpdate.cpp

## Purpose
Handles assisted targeting behavior for game objects, allowing external influences to command attacks beyond normal targeting range.

## Responsibilities
- Manages weapon lock states for assisted attacks
- Creates visual feedback lasers during assisted targeting
- Checks if an object is free to assist (e.g., not under construction)
- Processes assisted attack requests from other objects
- Handles module data parsing and serialization

## Key Types
- `AssistedTargetingUpdateModuleData` (Class): Stores configuration for assisted targeting (clip size, weapon slot, laser templates)
- `AssistedTargetingUpdate` (Class): Implements assisted targeting logic for game objects

## Key Functions
### `buildFieldParse`
- Purpose: Registers module data fields for INI parsing
- Calls: `UpdateModuleData::buildFieldParse`

### `isFreeToAssist`
- Purpose: Checks if the object can perform assisted attacks
- Calls: `Object::isAbleToAttack`, `Object::getCurrentWeapon`, `Weapon::getStatus`

### `assistAttack`
- Purpose: Executes an assisted attack on a target object
- Calls: `Object::setWeaponLock`, `AI::aiAttackObject`, `makeFeedbackLaser`

### `makeFeedbackLaser`
- Purpose: Creates visual laser effects between objects
- Calls: `TheThingFactory::newObject`, `Drawable::findClientUpdateModule`, `LaserUpdate::initLaser`

### `update`
- Purpose: Initializes laser templates during update
- Calls: `TheThingFactory::findTemplate`

## Globals
- `TheThingFactory` (ThingFactory*): Used to create/destroy objects and find templates
- `TheGameLogic` (GameLogic*): Used to destroy objects

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/Xfer.h`
- `GameLogic/Object.h`, `GameLogic/Weapon.h`, `GameLogic/WeaponSet.h`
- `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/AssistedTargetingUpdate.h`, `GameLogic/Module/LaserUpdate.h`
