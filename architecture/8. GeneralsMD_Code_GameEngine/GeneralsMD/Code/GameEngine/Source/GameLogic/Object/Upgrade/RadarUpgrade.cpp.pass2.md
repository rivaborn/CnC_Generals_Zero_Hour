# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/RadarUpgrade.cpp - Enhanced Analysis

## Architectural Role
This file implements the radar upgrade system, bridging between object upgrades and player radar management. It handles state transitions during object capture/deletion and coordinates with the RadarUpdate module to extend radar range.

## Cross-References
### Incoming
- **UpgradeModule**: Base class for upgrade behavior
- **Player**: Called to add/remove radar facilities
- **RadarUpdate**: Found via `findUpdateModule` to extend radar range
- **Xfer/MultiIniFieldParse**: For serialization and INI parsing

### Outgoing
- **UpgradeModule**: Extended for base upgrade functionality
- **Player**: `addRadar`/`removeRadar` for radar management
- **RadarUpdate**: `extendRadar` to modify radar range

## Design Patterns
- **Template Method**: `upgradeImplementation` defines the radar-specific upgrade logic while deferring to base class for common behavior.
- **Observer**: `onCapture`/`onDelete` react to object state changes, modifying player radar state accordingly.
- **Composite**: RadarUpgrade is part of a larger object module hierarchy (UpgradeModule â RadarUpgrade).

*Not inferable*: No clear use of Strategy or Factory patterns in this file.
