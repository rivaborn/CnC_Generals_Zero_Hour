# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/NeutronBlastBehavior.h

## Purpose
Defines the neutron blast behavior module for the game, which destroys infantry units within a blast radius.

## Responsibilities
- Manages neutron blast behavior parameters (radius, airborne/ally targeting)
- Handles object destruction logic
- Provides update and die callbacks for game loop integration
- Parses configuration data from INI files

## Key Types
- **NeutronBlastBehaviorModuleData (Class)**: Holds configuration data for the blast behavior
- **NeutronBlastBehavior (Class)**: Implements the neutron blast behavior module
- **NeutronBlastBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **NeutronBlastBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### NeutronBlastBehaviorModuleData::buildFieldParse
- Purpose: Registers INI field parsers for module data
- Calls: UpdateModuleData::buildFieldParse

### NeutronBlastBehavior::update
- Purpose: Updates the blast behavior state each frame
- Calls: Not inferable

### NeutronBlastBehavior::onDie
- Purpose: Handles cleanup when the behavior owner dies
- Calls: Not inferable

### NeutronBlastBehavior::neutronBlastToObject
- Purpose: Applies blast damage to a specific object
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/DieModule.h`
- `GameLogic/Module/UpdateModule.h`
- `MultiIniFieldParse`, `INI` namespaces
- `Thing`, `Object`, `DamageInfo` classes
- Memory pool and module macro systems
