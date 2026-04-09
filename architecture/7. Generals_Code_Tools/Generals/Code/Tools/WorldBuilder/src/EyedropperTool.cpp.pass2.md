# Generals/Code/Tools/WorldBuilder/src/EyedropperTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the eyedropper tool in WorldBuilder, a terrain editing utility. It bridges user input (mouse clicks) with terrain material management, enabling texture sampling for map creation.

## Cross-References
### Incoming
- **WorldBuilderDoc**: Calls `mouseDown` to handle user input.
- **WorldBuilderView**: Provides view-to-document coordinate conversion in `mouseDown`.
- **MainFrm**: Invoked via `activate` to display the terrain material panel.

### Outgoing
- **TerrainMaterial**: Updates foreground texture via `setFgTexClass`.
- **DrawObject**: Toggles brush feedback during tool activation.
- **WHeightMapEdit**: Retrieves texture class data for sampled terrain.

## Design Patterns
- **Command Pattern**: Encapsulates tool behavior (e.g., `mouseDown`) as methods, enabling dynamic switching of tools.
- **Observer Pattern**: Implicitly notifies `TerrainMaterial` of texture changes, decoupling the eyedropper from material logic.
- **Strategy Pattern**: Part of a tool hierarchy where `EyedropperTool` extends a base `Tool` class, allowing interchangeable tool behaviors.

*Not inferable*: No explicit use of factories, decorators, or state patterns.
