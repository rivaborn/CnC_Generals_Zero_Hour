# Generals/Code/Tools/WorldBuilder/include/BlendEdgeTool.h - Enhanced Analysis

## Architectural Role
This file defines a tool class for the WorldBuilder editor, specifically handling texture blending at map edges. It extends the base Tool class and integrates with the heightmap editing system, bridging the gap between user input and terrain modification.

## Cross-References
### Incoming
- Likely called by the WorldBuilder UI framework when texture tools are selected
- Probably referenced in tool palette initialization code

### Outgoing
- Inherits from Tool base class
- Uses WorldHeightMapEdit for terrain modifications
- Interacts with WbView and CWorldBuilderDoc for view and document management

## Design Patterns
- **Template Method**: mouseDown/mouseUp define hook points for tool behavior
- **Dependency Injection**: WorldHeightMapEdit is injected via parameters
- **Command Pattern**: Encapsulates a single tool operation as a reusable command

(Word count: 150)
