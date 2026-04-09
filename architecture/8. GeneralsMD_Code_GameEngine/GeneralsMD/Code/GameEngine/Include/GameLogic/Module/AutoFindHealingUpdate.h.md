# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AutoFindHealingUpdate.h

## Purpose
Defines the AutoFindHealingUpdate module for handling wounded idle infantry finding healing units or structures.

## Responsibilities
- Manages healing behavior for wounded infantry
- Scans for closest healing targets
- Controls update timing via frame intervals
- Handles module data configuration

## Key Types
- **AutoFindHealingUpdateModuleData (Class)**: Stores module configuration parameters
- **AutoFindHealingUpdate (Class)**: Main update module implementing healing logic
- **AutoFindHealingUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **ThingTemplate (Class)**: Forward reference to game object template
- **WeaponTemplate (Class)**: Forward reference to weapon template

## Key Functions
### AutoFindHealingUpdate::onObjectCreated
- Purpose: Initializes module when object is created
- Calls: Not inferable

### AutoFindHealingUpdate::update
- Purpose: Handles periodic healing target scanning
- Calls: scanClosestTarget

### AutoFindHealingUpdate::scanClosestTarget
- Purpose: Finds closest available healing target
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/KindOf.h
- GameLogic/Module/UpdateModule.h
- ModuleData (base class)
- UpdateModule (base class)
- Thing (forward reference)
- MultiIniFieldParse (used in buildFieldParse)
