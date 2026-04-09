# Generals/Code/Tools/WorldBuilder/include/wbview.h - Enhanced Analysis

## Architectural Role
This file defines the base view class for WorldBuilder, bridging MFC's document-view architecture with the game's spatial editing needs. It abstracts input handling, rendering, and coordinate transformations, serving as the foundation for both 2D and 3D map editors.

## Cross-References
### Incoming
- Derived classes (e.g., 2D/3D view implementations) override virtual methods
- WorldBuilder document classes use this for view coordination
- Tool classes reference picking and feedback methods

### Outgoing
- Calls into `CWorldBuilderDoc` for document access
- Uses `WorldHeightMapEdit` for terrain manipulation
- Interacts with `MapObject` hierarchy for selection logic

## Design Patterns
- **Template Method**: Virtual methods like `OnDraw` and coordinate transforms define hooks for derived classes
- **Observer**: View reacts to document changes via `invalObjectInView`/`invalidateCellInView`
- **Strategy**: Picking constraints (`m_pickConstraint`) allow runtime behavior modification

*Not inferable*: Concrete factory usage or visitor patterns.
