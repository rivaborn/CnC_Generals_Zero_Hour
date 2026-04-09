# Generals/Code/Tools/WorldBuilder/include/OpenMap.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for map selection in WorldBuilder, bridging the MFC dialog framework with the game's map loading system. It encapsulates the file browser functionality specific to map assets, distinguishing between system and user directories.

## Cross-References
### Incoming
- Likely called by `WorldBuilder`'s main frame or document classes when "Open Map" is invoked
- May be referenced by other tool dialogs needing map selection functionality

### Outgoing
- Interacts with MFC's `CDialog` and file system APIs
- Probably calls into `WorldBuilder`'s map loading subsystem (not shown in header)

## Design Patterns
- **MVC**: The dialog acts as the controller for map selection, with the listbox as the view
- **Strategy**: Directory switching (`OnSystemMaps`/`OnUserMaps`) suggests a strategy pattern for map source selection
- **Observer**: Event handlers (`OnBrowse`, `OnDblclkOpenList`) implement observer pattern for UI interactions

*Not inferable*: No clear use of factory, decorator, or visitor patterns in the header.
