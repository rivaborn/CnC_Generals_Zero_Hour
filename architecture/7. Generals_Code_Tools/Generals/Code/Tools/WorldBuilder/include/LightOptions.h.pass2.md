# Generals/Code/Tools/WorldBuilder/include/LightOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI dialog for light editing in WorldBuilder, bridging the MFC-based UI layer with the game's lighting system. It serves as a controller for light properties, coordinating between user input and the underlying MapObject system.

## Cross-References
### Incoming
- **GlobalLightOptions.h**: Uses `applyAngle`, `applyColor`, and slider-related methods to propagate UI changes to the lighting system.
- **MFC framework**: Inherits from `COptionsPanel` and uses MFC dialog mechanisms (`DoDataExchange`, message handlers).

### Outgoing
- **MapObject system**: Interacts with selected lights via `getSingleSelectedLight()`.
- **UI update system**: Calls `updateTheUI()` to synchronize the dialog with current light settings.

## Design Patterns
- **Singleton-like access**: Uses `m_staticThis` to provide global access to the dialog instance, enabling static update methods.
- **Observer pattern**: The dialog observes light selection changes (via `update()`) and updates its UI accordingly.
- **Model-View separation**: The dialog (view) updates based on the selected `MapObject` (model), though the separation isn't strictly enforced.
