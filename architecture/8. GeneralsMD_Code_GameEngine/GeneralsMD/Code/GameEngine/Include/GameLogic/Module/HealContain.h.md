# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HealContain.h

## Purpose
Defines the healing container module for the game, which heals contained units over time.

## Responsibilities
- Extends `OpenContain` to provide healing functionality
- Manages healing timing via `m_framesForFullHeal`
- Implements healing logic for contained objects
- Provides module data parsing and initialization

## Key Types
- **HealContainModuleData (Class)**: Module data containing healing timing parameter
- **HealContain (Class)**: Healing container implementation
- **HealContainMagicEnum (Enum)**: Not inferable (empty)
- **HealContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### HealContainModuleData::buildFieldParse
- Purpose: Parses module data fields from configuration
- Calls: Not inferable

### HealContain::update
- Purpose: Updates healing container state each frame
- Calls: Not inferable

### HealContain::doHeal
- Purpose: Applies healing to a contained object
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/OpenContain.h`
- Memory pool and module macros (SAGE engine internals)
- `MultiIniFieldParse` for configuration parsing
