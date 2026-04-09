# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DamDie.h

## Purpose
Defines the `DamDie` module for handling the destruction logic of the water dam in the game.

## Responsibilities
- Declares the `DamDieModuleData` class for module configuration.
- Declares the `DamDie` class for dam destruction behavior.
- Provides memory management macros for object pooling.
- Defines module creation and serialization macros.

## Key Types
- **DamDieModuleData (Class)**: Holds data for the dam destruction module.
- **DamDie (Class)**: Implements the dam destruction logic.
- **DamDieMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **DamDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### DamDieModuleData::buildFieldParse
- Purpose: Registers module data fields for parsing.
- Calls: Not inferable (likely calls `MultiIniFieldParse` methods).

### DamDie::onDie
- Purpose: Handles the dam's destruction logic when it dies.
- Calls: Not inferable (likely calls base class methods).

## Globals
- None

## Dependencies
- `DieModule.h` (base class)
- `MultiIniFieldParse` (for field parsing)
- Memory pool and module macros (internal SAGE engine utilities)
