# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DRadioButton.cpp - Enhanced Analysis

## Architectural Role
This file implements the rendering layer for radio button UI controls in the SAGE engine's W3D device layer. It bridges the abstract UI window system with the concrete rendering pipeline, handling both simple colored and image-based radio button representations.

## Cross-References
### Incoming
- `GadgetRadioButton.h` (header) - Defines the interface this implementation satisfies
- `W3DGadget.h` - Likely registers this as a gadget type in the W3D system
- UI event handlers (not shown) - Call the draw functions during UI rendering passes

### Outgoing
- `GameWindowManager.h` - Uses `TheWindowManager` for primitive drawing operations
- `W3DDisplay.h` - Uses `TheDisplay` for clipping region management
- `DisplayString` class - For text rendering and measurement

## Design Patterns
- **Strategy Pattern**: The two draw functions (`W3DGadgetRadioButtonDraw` and `W3DGadgetRadioButtonImageDraw`) represent different rendering strategies that can be selected at runtime.
- **State Pattern**: Visual appearance changes based on window state flags (enabled/disabled/highlighted/selected), with conditional logic routing to appropriate color/image resources.
- **Composite Pattern**: The image-based rendering (`W3DGadgetRadioButtonImageDraw`) treats the radio button as a composite of left/center/right image segments, handling the tiling of the center portion.
