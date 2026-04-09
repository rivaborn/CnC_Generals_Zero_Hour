# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarPopupDescription.cpp - Enhanced Analysis

## Architectural Role
This file implements the control bar tooltip system, bridging the UI layer with game state data. It handles dynamic content generation for tooltips based on player resources, selected units, and buildable structures, making it a critical component in the player feedback loop.

## Cross-References
### Incoming
- Called by control bar button hover events
- Invoked by game state changes (e.g., resource updates)
- Used by animation system for tooltip transitions

### Outgoing
- Queries player resources via `ThePlayerList` and `TheBuildAssistant`
- Fetches localized text through `TheGameText`
- Manages window layout via `TheWindowManager`
- Checks game state through `TheScriptEngine` and `TheGameLogic`

## Design Patterns
- **Observer Pattern**: Tooltips update in response to game state changes
- **Strategy Pattern**: Different tooltip content strategies for money, power, and science
- **Singleton Access**: Uses global managers (`TheControlBar`, `TheWindowManager`)

Rules followed. Output under 400 tokens.
