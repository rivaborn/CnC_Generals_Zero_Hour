# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/OverchargeBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the power plant overcharge system, a core gameplay mechanic that temporarily boosts power output at the cost of structural integrity. It bridges the power management system with object behavior, handling state transitions, health penalties, and player notifications.

## Cross-References
### Incoming
- Power plant objects (likely in `PowerPlant.cpp`) call `enable()` to activate/deactivate overcharge
- Player capture system calls `onCapture()` to transfer power bonuses
- Save/load system calls `xfer()` and `loadPostProcess()`

### Outgoing
- Calls `Player::addPowerBonus()`/`removePowerBonus()` to modify player power economy
- Uses `PowerPlantUpdateInterface` to control visual rod extension
- Interacts with `BodyModule` for health management
- Triggers UI messages via `TheInGameUI` and radar events via `TheRadar`

## Design Patterns
- **State Pattern**: Manages overcharge active/inactive states with clear transition logic
- **Observer Pattern**: Notifies player systems (power economy, UI) of state changes
- **Strategy Pattern**: Health drain calculation is delegated to module data configuration

*Not inferable*: No clear use of Visitor or Factory patterns in this file.
