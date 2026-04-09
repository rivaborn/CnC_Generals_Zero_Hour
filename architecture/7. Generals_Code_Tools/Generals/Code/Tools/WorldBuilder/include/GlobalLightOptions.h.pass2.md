# Generals/Code/Tools/WorldBuilder/include/GlobalLightOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for global lighting controls in WorldBuilder, bridging the gap between user input and the underlying lighting system. It encapsulates the modeless dialog behavior and slider interactions that modify scene lighting parameters.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main UI framework to spawn the lighting dialog
- Uses `WBPopupSliderButton` and `CButtonShowColor` components (included headers)

### Outgoing
- Interacts with the W3D rendering system to apply lighting changes (via `applyAngle`/`applyColor`)
- Depends on `PopupSliderOwner` interface for slider behavior

## Design Patterns
- **Model-View-Controller (MVC)**: Separates lighting data (model) from UI controls (view) and event handlers (controller)
- **Observer Pattern**: Slider callbacks (`PopSliderChanged`) react to user input changes
- **Strategy Pattern**: Different lighting scopes (terrain/objects/both) are selected via radio buttons, altering behavior

Rules followed. Output under 400 tokens.
