# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLocaleSelectPopup.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI and logic for the Westwood Online (WOL) locale selection popup, bridging the GameSpy networking layer with the game's UI system. It handles user interaction for locale selection and propagates changes to GameSpy preferences and player stats.

## Cross-References
### Incoming
- Called by the window manager when the locale selection popup is created/destroyed
- Invoked by GameSpy overlay when locale selection is triggered

### Outgoing
- Interacts with `GameSpyPSMessageQueue` for preference updates
- Uses `GameSpyMiscPreferences` for persistence
- Relies on `WindowManager` for window lifecycle
- Depends on `GameText` for localization strings

## Design Patterns
- **Observer Pattern**: The popup registers callbacks for window events (create/destroy/input)
- **Command Pattern**: Locale selection triggers a chain of commands (preference update, stats update, overlay close)
- **Singleton Access**: Uses global singletons (`TheGameSpyPSMessageQueue`, `TheWindowManager`) for subsystem access

*Not inferable*: No clear use of Factory, Strategy, or State patterns in this file.
