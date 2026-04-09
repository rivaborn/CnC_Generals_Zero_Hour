# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/TextEntryProperties.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for configuring text entry gadgets in the GUI editor tool. It bridges the editor's property system with the runtime text entry gadget implementation, enabling visual editing of text input controls.

## Cross-References
### Incoming
- **GUIEdit main module**: Likely calls `InitTextEntryPropertiesDialog` when user selects a text entry gadget for editing
- **Property system**: Uses `HandleCommonDialogMessages` and `SaveCommonDialogProperties` from the shared property dialog infrastructure

### Outgoing
- **GadgetTextEntry system**: Directly manipulates text entry gadget properties via `GadgetTextEntrySet*`/`Get*` functions
- **Image/Color system**: Uses `StoreImageAndColor` and `GetStateInfo` for state-specific visual properties
- **Dialog infrastructure**: Relies on `CommonDialogInitialize` and `SwitchToState` for standard dialog behavior

## Design Patterns
- **State Pattern**: Manages different visual states (enabled/disabled/highlighted) for text entry gadgets
- **Property Bag Pattern**: Uses `ImageAndColorInfo` and `EntryData` structs to bundle related properties together
- **Callback Handler**: Implements the classic Windows dialog callback pattern for event handling
