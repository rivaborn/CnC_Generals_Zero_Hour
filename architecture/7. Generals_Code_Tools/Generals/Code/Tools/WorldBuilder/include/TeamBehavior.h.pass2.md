# Generals/Code/Tools/WorldBuilder/include/TeamBehavior.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for team AI behavior configuration in WorldBuilder, bridging the gap between the editor's property page system and the underlying team behavior scripting system. It encapsulates the dialog logic for modifying team behavior scripts, making it a critical component in the WorldBuilder's modding toolchain.

## Cross-References
### Incoming
- Likely called by WorldBuilder's property page manager when team behavior settings need to be edited
- May be referenced by team/unit configuration dialogs that need to expose behavior options

### Outgoing
- Calls into the `Dict` class for script data management
- Interacts with MFC's `CPropertyPage` and dialog control mechanisms
- References behavior script names via `NameKeyType`, suggesting integration with the scripting system

## Design Patterns
- **Property Page Pattern**: Inherits from `CPropertyPage` to integrate with MFC's property sheet framework, allowing behavior configuration to be part of a larger settings dialog
- **Data Transfer Object**: Uses `Dict` to manage script data, separating UI concerns from behavior logic
- **Event Handling**: Uses MFC message map for UI event routing, typical of Windows dialog-based applications

*Not inferable*: Specific scripting system integration details or how behavior scripts are executed at runtime.
