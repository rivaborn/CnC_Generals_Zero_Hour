# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RiderChangeContain.h - Enhanced Analysis

## Architectural Role
This file defines the `RiderChangeContain` module, a specialized transport container for units that dynamically switch riders (e.g., combat bikes). It extends the base `TransportContain` class to handle rider-specific logic, such as validation, capture handling, and exit management, integrating tightly with the game's object containment and UI systems.

## Cross-References
### Incoming
- **GameLogic/Module/TransportContain.h**: Inherits from `TransportContain`, indicating this is a specialized transport container.
- **INI parsing system**: Uses `MultiIniFieldParse` and `INI` for configuration, suggesting tight coupling with the game's data-driven architecture.
- **UI/ControlBar**: Called by UI systems to display container contents (e.g., `isDisplayedOnControlBar`).

### Outgoing
- **Object/Thing systems**: Interacts with `Object` and `Thing` for containment logic.
- **Player system**: Handles ownership changes (e.g., `onCapture`).
- **ExitDoor management**: Manages exit doors for rider egress (e.g., `reserveDoorForExit`).

## Design Patterns
- **Template Method**: Overrides virtual methods like `isValidContainerFor` and `update` to extend base transport behavior.
- **Data-Driven Design**: Uses `RiderInfo` struct and INI parsing to configure rider types, enabling modding.
- **Strategy Pattern**: Encapsulates rider-specific logic (e.g., `killRidersWhoAreNotFreeToExit`) for dynamic behavior.
