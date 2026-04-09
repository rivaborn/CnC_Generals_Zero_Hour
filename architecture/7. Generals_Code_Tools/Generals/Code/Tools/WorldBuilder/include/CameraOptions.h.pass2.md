# Generals/Code/Tools/WorldBuilder/include/CameraOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for camera manipulation in WorldBuilder, bridging MFC dialog handling with game-specific camera controls. It implements the PopupSliderOwner interface, indicating tight integration with WorldBuilder's slider-based input system.

## Cross-References
### Incoming
- WorldBuilder's main UI framework (likely calls `CameraOptions` constructor and message handlers)
- WBPopupSlider system (uses `PopupSliderOwner` interface)

### Outgoing
- Directly manipulates camera state (via `applyCameraPitch` and `update`)
- Uses MFC's `CDialog` infrastructure for UI management

## Design Patterns
- **Adapter Pattern**: Bridges MFC's `CDialog` with game-specific camera controls
- **Observer Pattern**: Implements slider change callbacks (`PopSliderChanged`, `PopSliderFinished`)
- **Template Method**: Overrides MFC virtuals (`DoDataExchange`, `OnInitDialog`) for custom behavior

*Not inferable*: Exact camera state management pattern (likely singleton or service locator).
