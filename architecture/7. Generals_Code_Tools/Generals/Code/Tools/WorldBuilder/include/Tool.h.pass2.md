# Generals/Code/Tools/WorldBuilder/include/Tool.h - Enhanced Analysis

## Architectural Role
This file defines the abstract base class for all terrain editing tools in the WorldBuilder editor, serving as the core interface for tool behavior, cursor management, and terrain manipulation. It bridges the UI layer (cursor handling) with the document/model layer (terrain data).

## Cross-References
### Incoming
- Derived tool classes (BrushTool, RampTool, etc.) inherit and override virtual methods
- WorldBuilderView likely instantiates and manages Tool objects
- ToolManager (if exists) would use this interface for tool switching

### Outgoing
- References CWorldBuilderDoc and WbView for document/view interaction
- Uses Lib\BaseType.h and Common/STLTypedefs.h for core types
- Static methods imply usage by derived classes for brush calculations

## Design Patterns
- **Template Method**: Virtual mouse event handlers define a workflow that derived classes customize
- **Strategy**: Tools are interchangeable strategies for terrain editing
- **Factory Method**: Tool creation likely delegated to derived classes (not shown here)

*Not inferable*: Concrete factory or tool registry implementation.
