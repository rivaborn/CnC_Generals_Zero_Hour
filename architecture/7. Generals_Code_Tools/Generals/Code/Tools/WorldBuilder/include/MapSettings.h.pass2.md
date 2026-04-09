# Generals/Code/Tools/WorldBuilder/include/MapSettings.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for WorldBuilder's map configuration, bridging MFC dialog infrastructure with game-specific map properties. It encapsulates the settings dialog used during map creation/editing, exposing controls for metadata (title), environmental settings (time/weather), and technical parameters (compression).

## Cross-References
### Incoming
- `WorldBuilder.cpp` (main tool entry point) - instantiates and displays the dialog
- `MapDocument` class - likely uses the collected settings during map save/export
- MFC framework - handles base dialog functionality and message routing

### Outgoing
- Calls into MFC's `CDialog`, `CDataExchange`, and message map system
- Likely interacts with `MapDocument` to apply settings to the current map
- May reference `MapInfo` structures for validation of entered values

## Design Patterns
- **MVC (Model-View-Controller)**: The dialog acts as the view/controller, with `MapDocument` serving as the model
- **Observer Pattern**: Event handlers (`OnChange*`) react to UI changes, implying a push model for settings updates
- **Template Method**: `DoDataExchange` follows MFC's template method pattern for data binding

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns in this header alone.
