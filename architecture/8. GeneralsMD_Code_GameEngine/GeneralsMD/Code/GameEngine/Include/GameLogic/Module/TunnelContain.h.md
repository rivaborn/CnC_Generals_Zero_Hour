# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TunnelContain.h

## Purpose
Defines the `TunnelContain` module, a specialized container for managing units in a tunnel network, overriding storage and capacity logic.

## Responsibilities
- Manages unit containment via the owning player's `TunnelTracker`.
- Handles healing, capture, and destruction of contained units.
- Provides tunnel-specific behavior (e.g., immunity to clear-building attacks).
- Integrates with the game's module system via `CreateModuleInterface`.

## Key Types
- **TunnelContainModuleData (Class)**: Module data with healing time and allowed unit types.
- **TunnelContain (Class)**: Tunnel container implementation, extending `OpenContain`.
- **TunnelContainMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **Team (Class)**: External reference for team management.

## Key Functions
### `TunnelContainModuleData::buildFieldParse`
- Purpose: Registers INI fields for module data parsing.
- Calls: `OpenContainModuleData::buildFieldParse`.

### `TunnelContain::onContaining`
- Purpose: Handles unit containment events.
- Calls: Not inferable (implementation in `.cpp`).

### `TunnelContain::update`
- Purpose: Updates healing state of contained units.
- Calls: Not inferable.

### `TunnelContain::onDie`
- Purpose: Handles destruction, killing contained units.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- **Includes**: `OpenContain.h`, `HealContain.h`, `DieModule.h`, `CreateModule.h`, `GameMemory.h`.
- **External Symbols**: `Team`, `MultiIniFieldParse`, `INI`, `KINDOF_INFANTRY`, `MODULEINTER
