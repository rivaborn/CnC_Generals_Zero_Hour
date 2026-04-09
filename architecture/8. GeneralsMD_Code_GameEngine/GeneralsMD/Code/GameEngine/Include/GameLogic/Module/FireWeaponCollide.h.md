# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireWeaponCollide.h

## Purpose
Defines a game logic module for firing weapons when collisions occur.

## Responsibilities
- Handles weapon firing on object collision
- Manages collision weapon template and status filters
- Controls whether weapon fires once or repeatedly

## Key Types
- **FireWeaponCollideModuleData (Class)**: Stores weapon template and collision status filters
- **FireWeaponCollide (Class)**: Implements collision-based weapon firing logic
- **FireWeaponCollideMagicEnum (Enum)**: Not inferable
- **FireWeaponCollide_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### FireWeaponCollideModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

### FireWeaponCollide::onCollide
- Purpose: Handles collision events and triggers weapon firing
- Calls: Not inferable

### FireWeaponCollide::shouldFireWeapon
- Purpose: Determines if weapon should fire based on collision conditions
- Calls: Not inferable

## Globals
- None

## Dependencies
- `CollideModule.h`
- `GameLogic/Weapon.h`
- `Object` class (forward reference)
- `WeaponTemplate` class
- `MultiIniFieldParse` class
- `Coord3D` struct
- `Thing` class
- `ModuleData` class
