# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/NewLayoutDialog.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for initiating a new layout in the GUI editor tool, bridging user input with the core editor functionality. It demonstrates the separation between tooling UI and game engine logic, with the dialog acting as a thin wrapper around `TheEditor->newLayout()`.

## Cross-References
### Incoming
- Called by Windows message loop (via `DialogBox` or similar) when the new layout dialog is invoked
- Likely referenced in menu handlers or toolbar callbacks in the GUI editor

### Outgoing
- Calls `TheEditor->newLayout()` to trigger layout creation in the core editor
- Uses Windows API (`SetFocus`, `GetDlgItem`, `EndDialog`) for dialog management
- Depends on `EditWindow.h` for the global editor instance

## Design Patterns
- **Dialog Controller**: The `NewLayoutDialogProc` handles all dialog-related logic, encapsulating UI behavior
- **Global Accessor**: Uses `TheEditor` singleton pattern for editor state management (common in tooling)
- **Command Pattern**: The OK button action delegates to `newLayout()`, separating UI from business logic

*Not inferable*: No clear use of observer pattern or other complex patterns in this simple dialog implementation.
