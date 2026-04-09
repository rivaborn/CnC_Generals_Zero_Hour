# Generals/Code/Tools/WorldBuilder/src/EditParameter.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central UI controller for parameter editing in WorldBuilder, bridging the gap between the tool's MFC-based UI and the game's parameter system. It acts as a factory for specialized parameter editors while handling common validation and preview functionality.

## Cross-References
### Incoming
- Called by WorldBuilder's main editing interface when parameters need modification
- Used by specialized editors (EditCoordParameter, EditObjectParameter) as base functionality

### Outgoing
- Dispatches to MFC dialog classes (CColorDialog) for standard UI controls
- Queries game systems (TheGameText, TheAudio) for runtime data
- Interacts with game logic (AI moods, radar events) through shared enums

## Design Patterns
- **Factory Method**: The `edit()` function acts as a factory, creating appropriate editor dialogs based on parameter type
- **Adapter**: Converts between UI control formats (e.g., color dialog's 00bbggrr to game's aarrggbb)
- **Strategy**: Different handling for each parameter type (angle conversion, localized text loading) embedded in switch cases

*Not inferable*: No clear use of Observer or Command patterns despite event-driven UI.
