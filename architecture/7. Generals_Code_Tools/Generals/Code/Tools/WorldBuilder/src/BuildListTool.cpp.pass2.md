# Generals/Code/Tools/WorldBuilder/src/BuildListTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the building placement and manipulation tool for WorldBuilder, bridging the UI layer with the 3D rendering system. It handles user input for building selection, placement, movement, and rotation while coordinating with the view system for visual feedback.

## Cross-References
### Incoming
- **Tool Framework**: Uses base `Tool` class for common tool behavior
- **View System**: Called by `WbView3d` and `WbView` for input handling
- **Document System**: Integrated with `CWorldBuilderDoc` for scene management

### Outgoing
- **UI System**: Controls `PickUnitDialog` and `CMainFrame` dialogs
- **Rendering**: Interfaces with `DrawObject` and `WbView3d` for visual updates
- **Game Logic**: Uses `ObjectOptions` and `BuildList` for building data

## Design Patterns
- **Command Pattern**: Encapsulates building operations (place/move/rotate) as discrete actions
- **Observer Pattern**: Listens to mouse events and updates view state accordingly
- **State Pattern**: Manages different tool states (active/inactive, moving/rotating) implicitly through flags

*Not inferable*: No explicit use of Factory, Strategy, or Visitor patterns detected.
