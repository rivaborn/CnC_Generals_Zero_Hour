# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DamageModule.h

## Purpose
Defines the damage handling module interface and base class for game objects in the SAGE engine.

## Responsibilities
- Declares the `DamageModuleInterface` for damage-related callbacks.
- Provides `DamageModuleData` for configuration parsing.
- Implements `DamageModule` as an abstract base class for damage behavior.
- Manages memory allocation via `MEMORY_POOL_GLUE_ABC`.

## Key Types
- **BodyDamageType (Enum)**: Not inferable (forward-declared).
- **DamageModuleInterface (Class)**: Interface for damage/healing callbacks.
- **DamageModuleData (Class)**: Module data with INI parsing support.
- **DamageModule (Class)**: Abstract base class for damage behavior modules.
- **DamageModuleMagicEnum (Enum)**: Not inferable (forward-declared).
- **DamageModule_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (forward-declared).

## Key Functions
### `DamageModuleInterface::onDamage`
- Purpose: Handles damage application.
- Calls: None (pure virtual).

### `DamageModuleInterface::onHealing`
- Purpose: Handles healing application.
- Calls: None (pure virtual).

### `DamageModuleInterface::onBodyDamageStateChange`
- Purpose: Notifies on body damage state changes.
- Calls: None (pure virtual).

### `DamageModuleData::buildFieldParse`
- Purpose: Registers INI field parsing rules.
- Calls: `BehaviorModuleData::buildFieldParse`.

### `DamageModule::onDamage`
- Purpose: Abstract damage callback (must be implemented by derived classes).
- Calls: None (pure virtual).

### `DamageModule::onHealing`
- Purpose: Abstract healing callback (must be implemented by derived classes).
- Calls: None (pure virtual).

### `
