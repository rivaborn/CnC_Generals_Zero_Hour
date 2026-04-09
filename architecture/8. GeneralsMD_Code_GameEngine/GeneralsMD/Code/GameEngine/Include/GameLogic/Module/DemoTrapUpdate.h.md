# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DemoTrapUpdate.h

## Purpose
Defines the DemoTrapUpdate module for handling demo trap proximity triggering in the game.

## Responsibilities
- Manages demo trap behavior (proximity/manual detonation)
- Handles object creation and update logic
- Controls weapon slot management for different modes
- Implements detonation logic

## Key Types
- **DemoTrapUpdateModuleData (Class)**: Contains configuration data for demo traps (weapon templates, ranges, etc.)
- **DemoTrapUpdate (Class)**: Main update module class handling demo trap logic
- **DemoTrapUpdateMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **DemoTrapUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### DemoTrapUpdate::onObjectCreated
- Purpose: Initializes the demo trap when object is created
- Calls: Not inferable

### DemoTrapUpdate::update
- Purpose: Handles periodic scanning for proximity triggers
- Calls: Not inferable

### DemoTrapUpdate::detonate
- Purpose: Triggers the demo trap detonation
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/KindOf.h`
- `GameLogic/Module/UpdateModule.h`
- `ModuleData` (base class)
- `UpdateModule` (base class)
- `WeaponTemplate`, `KindOfMaskType`, `WeaponSlotType`, `Real`, `UnsignedInt`, `Bool` (types)
