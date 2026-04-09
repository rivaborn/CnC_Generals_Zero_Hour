# GeneralsMD/Code/GameEngine/Source/Common/RTS/Energy.cpp - Enhanced Analysis

## Architectural Role
This file implements the core energy management system for the RTS game, acting as a bridge between player resources and object templates. It handles dynamic power calculations, sabotage effects, and energy state serialization, critical for gameplay balance and persistence.

## Cross-References
### Incoming
- **Player.cpp**: Calls `onPowerBrownOutChange` when energy state changes
- **Object.cpp**: Invokes `objectEnteringInfluence`/`objectLeavingInfluence` during object lifecycle
- **GameLogic.cpp**: Uses `getProduction`/`getEnergySupplyRatio` for UI/hud updates
- **Xfer.cpp**: Serializes energy state via `xfer` method

### Outgoing
- **Player.h**: Accesses `m_owner->onPowerBrownOutChange()`
- **ThingTemplate.h**: Queries `getEnergyProduction()`/`getEnergyBonus()`
- **GameLogic.h**: Checks `TheGameLogic->getFrame()` for sabotage timing
- **PlayerList.h**: Resolves player ownership during deserialization

## Design Patterns
- **Observer Pattern**: Energy notifies owner (Player) of state changes via `onPowerBrownOutChange`
- **Resource Pool**: Manages energy as a shared resource with production/consumption tracking
- **Versioned Serialization**: Uses `XferVersion` for backward-compatible save/load (v1-v3)

*Not inferable*: No clear use of Strategy or Factory patterns in this file.
