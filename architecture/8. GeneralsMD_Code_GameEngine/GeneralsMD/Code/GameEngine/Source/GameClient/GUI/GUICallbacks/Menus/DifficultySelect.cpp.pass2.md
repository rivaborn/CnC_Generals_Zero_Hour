# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DifficultySelect.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for campaign difficulty selection, bridging the UI system with game preferences and campaign management. It handles user input, preference persistence, and game initialization flow.

## Cross-References
### Incoming
- Called by UI event system when difficulty menu is opened
- Invoked by `CampaignManager` when campaign difficulty needs selection

### Outgoing
- Calls `OptionPreferences` for persistence
- Uses `CampaignManager` to start campaigns
- Interacts with `WindowManager` for UI control
- References `ScriptEngine` for difficulty validation

## Design Patterns
- **Observer Pattern**: UI controls notify via callbacks when selected
- **Mediator Pattern**: Centralizes UI control coordination
- **Singleton Access**: Uses global managers (`TheWindowManager`, `TheCampaignManager`)

Rules followed. Output under 400 tokens.
