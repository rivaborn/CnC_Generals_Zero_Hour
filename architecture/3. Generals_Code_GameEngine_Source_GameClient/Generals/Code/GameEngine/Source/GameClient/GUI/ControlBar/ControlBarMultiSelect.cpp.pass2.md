# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarMultiSelect.cpp - Enhanced Analysis

## Architectural Role
This file implements the multi-select command UI logic in the ControlBar system, bridging the gap between unit selection (InGameUI) and command execution (GameClient). It dynamically filters and displays commands valid for all selected units, handling both command availability and visual feedback.

## Cross-References
### Incoming
- **ControlBar.cpp**: Calls `populateMultiSelect` and `updateContextMultiSelect` during selection updates
- **InGameUI.cpp**: Provides selected drawable list via `getAllSelectedDrawables()`
- **GameClient.cpp**: Uses `getCommandAvailability` for command state evaluation

### Outgoing
- **GadgetPushButton.h**: Uses `GadgetButtonGetData`/`SetVisualCheck` for button state management
- **GameWindow.h**: Manages window visibility/enablement via `winHide`/`winEnable`
- **ThingTemplate.h**: Accesses unit portraits through `getSelectedPortraitImage`

## Design Patterns
- **Strategy Pattern**: Command availability checks (`getCommandAvailability`) act as strategies for enabling/disabling buttons
- **Observer Pattern**: Reacts to selection changes from `TheInGameUI` (implicit global observer)
- **Null Object Pattern**: Uses `NULL` checks for missing commands/portraits (e.g., `m_commonCommands[i] == NULL`)

*Not inferable*: Exact command set resolution mechanism (`findCommandSet`) remains opaque.
