# Generals/Code/Libraries/Source/WWVegas/WW3D2/htree.h - Enhanced Analysis

## Architectural Role
This file defines the core skeletal animation hierarchy system (HTreeClass) for the W3D rendering pipeline. It bridges between static model data and dynamic animation systems, serving as the foundation for character/vehicle rigging in the game.

## Cross-References
### Incoming
- MeshClass (friend relationship) - likely uses HTree for rendering animated models
- Animation systems (HAnimClass, HAnimComboClass, HRawAnimClass) - apply motion to the hierarchy
- W3D file loading/saving infrastructure (ChunkLoadClass/ChunkSaveClass)

### Outgoing
- Matrix3D operations for transform calculations
- PivotClass for individual bone data storage
- WWDebug for assertions and debugging

## Design Patterns
- **Composite Pattern**: Hierarchy of pivots/bones forms a tree structure
- **Strategy Pattern**: Different update methods (Blend_Update, Combo_Update) provide varying animation strategies
- **Factory Methods**: Create_Morphed and Create_Interpolated as static factory methods for hierarchy manipulation

Rules followed. Analysis limited to 400 tokens.
