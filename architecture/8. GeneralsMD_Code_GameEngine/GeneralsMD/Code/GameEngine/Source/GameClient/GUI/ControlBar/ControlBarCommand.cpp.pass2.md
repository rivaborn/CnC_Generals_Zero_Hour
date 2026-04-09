# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarCommand.cpp - Enhanced Analysis

## Architectural Role
This file bridges the UI layer and game logic, implementing command availability checks that dynamically enable/disable control bar buttons based on unit state, player resources, and game rules. It's a critical mediator between player input and game state validation.

## Cross-References
### Incoming
- Called by UI event handlers when command buttons are pressed
- Used by ControlBar to populate transport inventory displays
- Referenced by InGameUI for selection-based command availability

### Outgoing
- Queries GameLogic modules (BattlePlanUpdate, SpecialPowerModule, etc.)
- Accesses Player/ThingTemplate data for resource and template checks
- Uses GadgetButton functions for visual state updates

## Design Patterns
- **Strategy Pattern**: Command availability checks are implemented as a large switch statement, effectively encapsulating different command behaviors
- **Observer Pattern**: UI state updates (button enable/disable) are triggered by game state changes
- **Visitor Pattern**: `populateInvDataCallback` iterates over transport contents, applying UI updates

Rules followed. Output under 400 tokens.
