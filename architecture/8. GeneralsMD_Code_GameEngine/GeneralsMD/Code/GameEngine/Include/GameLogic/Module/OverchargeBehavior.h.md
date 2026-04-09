# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OverchargeBehavior.h

## Purpose
Defines the OverchargeBehavior module, allowing objects to temporarily boost power output at the cost of health.

## Responsibilities
- Manages overcharge state (on/off)
- Handles health drain during overcharge
- Provides damage and update interfaces
- Supports module data configuration

## Key Types
- **OverchargeBehaviorModuleData (Class)**: Stores overcharge parameters (health drain rate, minimum health threshold).
- **OverchargeBehaviorInterface (Class)**: Abstract interface for overcharge control (toggle/enable/check status).
- **OverchargeBehavior (Class)**: Implements overcharge behavior, inheriting from UpdateModule and DamageModuleInterface.
- **OverchargeBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **OverchargeBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### OverchargeBehaviorModuleData::buildFieldParse
- Purpose: Registers module data fields for parsing.
- Calls: Not inferable.

### OverchargeBehavior::update
- Purpose: Updates overcharge state and drains health.
- Calls: Not inferable.

### OverchargeBehavior::onDamage
- Purpose: Handles damage events during overcharge.
- Calls: Not inferable.

### OverchargeBehavior::toggle
- Purpose: Toggles overcharge state.
- Calls: Not inferable.

### OverchargeBehavior::enable
- Purpose: Enables/disables overcharge.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `BehaviorModule.h`, `DamageModule.h`, `UpdateModule.h`
- `MultiIniFieldParse`, `Thing`, `ModuleData`, `DamageInfo`, `Player`, `Real`, `Bool`, `Int`
