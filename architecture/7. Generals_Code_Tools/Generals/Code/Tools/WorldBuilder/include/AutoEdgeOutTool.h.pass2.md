# Generals/Code/Tools/WorldBuilder/include/AutoEdgeOutTool.h - Enhanced Analysis

## Architectural Role
This file defines a terrain editing tool within WorldBuilder, extending the base Tool class to provide edge-blending functionality. It integrates with the WorldBuilder's terrain manipulation subsystem, specifically targeting heightmap modifications.

## Cross-References
### Incoming
- Likely called by WorldBuilder's tool management system (e.g., tool palette or command dispatcher)
- May be referenced in WorldBuilder's tool registration mechanism

### Outgoing
- Inherits from Tool.h, implying usage of base tool functionality
- Interacts with WorldHeightMapEdit for actual terrain modifications
- Uses WbView and CWorldBuilderDoc for view/editor context

## Design Patterns
- **Template Method**: mouseDown() and activate() are virtual, suggesting a base Tool class defines the algorithm skeleton
- **Dependency Injection**: WorldHeightMapEdit is injected via parameters in mouseDown(), decoupling edge logic from tool implementation
- **Not inferable**: No clear use of other patterns without implementation details
