# Generals/Code/Tools/WorldBuilder/include/ScriptProperties.h - Enhanced Analysis

## Architectural Role
This header defines the `ScriptProperties` dialog class, part of WorldBuilder's editor UI for managing script metadata and execution parameters. It bridges the MFC-based UI layer with the game's scripting system, enabling level designers to configure script behavior without direct code access.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main editor UI framework (e.g., property sheet managers)
- Script object instances (from `Script.h`) are passed via `setScript()`

### Outgoing
- Interacts with MFC's `CPropertyPage` base class for dialog functionality
- References `Script` class for script object manipulation
- Uses MFC's DDX/DDV mechanism for UI-data binding

## Design Patterns
- **Property Page Pattern**: Extends `CPropertyPage` to encapsulate script properties editing in a reusable tabbed interface.
- **Observer Pattern**: UI controls notify the dialog of changes (e.g., `OnChangeScriptName`), which then updates the underlying `Script` object.
- **Strategy Pattern**: Script timing/trigger options (e.g., `OnEveryFrame`, `OnEverySecond`) suggest configurable execution strategies for scripts.

*Not inferable*: Exact data flow between UI controls and `Script` object (handled in `DoDataExchange`).
