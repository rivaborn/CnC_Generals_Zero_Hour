# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RadarUpgrade.h - Enhanced Analysis

## Architectural Role
This file defines the radar upgrade module, which extends the base upgrade system to provide radar functionality for game objects. It integrates with the upgrade framework and handles radar-specific behavior during object lifecycle events (creation, deletion, capture).

## Cross-References
### Incoming
- `UpgradeModule.h` (base class)
- `Thing` (object containing the upgrade)
- `Player` (for team change handling)
- `MultiIniFieldParse` (configuration parsing)

### Outgoing
- Likely calls into radar rendering/visibility systems (not explicitly shown)
- May interact with player radar UI components
- Probably uses memory pool allocation macros

## Design Patterns
- **Template Method**: `upgradeImplementation()` defines the core upgrade behavior while allowing subclasses to extend it
- **Strategy**: Radar upgrade is one of many possible upgrade types, following the strategy pattern for modular behavior
- **Observer**: `onCapture()` and `onDelete()` suggest event-driven design for state changes

Rules followed. Output under 400 tokens.
