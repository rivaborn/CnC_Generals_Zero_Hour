# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CommandButtonHuntUpdate.h

## Purpose
Defines a game logic module for handling wounded infantry units seeking healing targets.

## Responsibilities
- Manages scan behavior for wounded units to find healers
- Updates unit state based on scan results
- Handles command button assignment for healing actions
- Provides hunt logic for special powers, weapons, and entry points

## Key Types
- **CommandButtonHuntUpdateModuleData (Class)**: Holds module configuration (scan frames, range)
- **CommandButtonHuntUpdate (Class)**: Main update module implementing hunt behavior
- **CommandButtonHuntUpdateMagicEnum (Enum)**: Not inferable (likely internal enum)
- **ThingTemplate (Class)**: Forward reference to game object template
- **WeaponTemplate (Class)**: Forward reference to weapon data

## Key Functions
### CommandButtonHuntUpdate::scanClosestTarget
- Purpose: Finds the nearest valid target for healing
- Calls: Not inferable

### CommandButtonHuntUpdate::huntSpecialPower
- Purpose: Handles hunting for special power targets
- Calls: Not inferable

### CommandButtonHuntUpdate::huntWeapon
- Purpose: Manages weapon-based hunting behavior
- Calls: Not inferable

### CommandButtonHuntUpdate::huntEnter
- Purpose: Implements entry point hunting logic
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/KindOf.h` (for KindOf types)
- `GameLogic/Module/UpdateModule.h` (base class)
- `ModuleData` (base class for module data)
- `Thing`, `CommandButton`, `AIUpdateInterface`, `MultiIniFieldParse` (external types)
