# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DPushButton.cpp - Enhanced Analysis

## Architectural Role
This file implements the rendering layer for push button UI elements within the W3DDevice subsystem, bridging the abstract Gadget system with concrete W3D rendering primitives. It handles both image-based and color-based button rendering, with special support for state transitions (enabled/disabled/selected) and advanced UI features like clocks and overlays.

## Cross-References
### Incoming
- Called by the Gadget system when rendering push buttons (likely from `Gadget::Draw` or similar)
- Used by UI layout code that needs to render buttons with specific states

### Outgoing
- Calls into `GadgetButtonGet*` functions for state-specific resources
- Uses `TheWindowManager` and `TheDisplay` singletons for rendering operations
- Interacts with `DisplayString` for text rendering

## Design Patterns
- **Strategy Pattern**: Different drawing methods (`W3DGadgetPushButtonImageDrawOne` vs `W3DGadgetPushButtonImageDrawThree`) are selected based on button configuration
- **Decorator Pattern**: Overlay images, clocks, and borders are added as optional decorations to base button rendering
- **State Pattern**: Button appearance changes based on internal state (enabled/disabled/selected) without modifying core drawing logic
