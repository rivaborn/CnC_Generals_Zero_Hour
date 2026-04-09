# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/RadioButtonProperties.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI configuration dialog for radio button gadgets in the GUI editor tool, bridging the editor's property system with the runtime gadget implementation. It handles serialization of radio button states (enabled/disabled/highlighted) and group management, which is critical for the editor's ability to modify UI elements while preserving runtime behavior.

## Cross-References
### Incoming
- Called by the GUI editor's property system when a radio button is selected for editing
- Uses `CommonDialogInitialize` from the editor framework for shared dialog initialization

### Outgoing
- Directly manipulates `GameWindow` objects via `GadgetRadioSet*` functions
- Recursively traverses the window hierarchy through `winGetChild`/`winGetNext`
- Interacts with the name key system (`TheNameKeyGenerator`) for resource management

## Design Patterns
- **Property Bag Pattern**: Uses `ImageAndColorInfo` structs to bundle related state properties
- **Visitor Pattern**: Recursively processes window hierarchy in `loadExistingGroupsCombo`
- **Command Pattern**: Dialog callbacks encapsulate UI state changes as discrete operations

Rules followed. Output under 400 tokens.
