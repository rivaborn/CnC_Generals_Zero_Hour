# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/StaticTextProperties.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for editing static text gadget properties in the GUI editor tool. It bridges the editor's property system with the runtime gadget implementation, allowing designers to configure text appearance and behavior.

## Cross-References
### Incoming
- Called by the GUI editor's property system when a static text gadget is selected for editing

### Outgoing
- Calls into `GadgetStaticText` class for getting/setting visual states
- Uses `Properties.h` helper functions for dialog state management
- Interacts with `TheEditor` singleton for accessing the current property target

## Design Patterns
- **Dialog Controller**: The callback function handles all dialog events and updates the target gadget
- **State Pattern**: Visual states (enabled/disabled/highlight) are managed through separate state objects
- **Mediator**: The dialog mediates between the UI and the gadget's underlying properties

Rules followed. Output under 400 tokens.
