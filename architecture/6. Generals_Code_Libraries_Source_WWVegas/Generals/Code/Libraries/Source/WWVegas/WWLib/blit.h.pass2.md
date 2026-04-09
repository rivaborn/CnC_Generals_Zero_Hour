# Generals/Code/Libraries/Source/WWVegas/WWLib/blit.h - Enhanced Analysis

## Architectural Role
This header defines the core blitting abstraction layer for the SAGE engine's rendering pipeline, bridging between low-level blitter implementations (in blitblit.h) and high-level surface operations. It serves as the primary interface for 2D graphics operations across the engine.

## Cross-References
### Incoming
- `Generals/Code/Libraries/Source/WWVegas/WWLib/blitblit.h` (assembly implementations)
- Various rendering subsystems (UI, W3D, particle effects) that need surface blitting
- Networking code for texture streaming/serialization

### Outgoing
- `blitter.h` (base blitter interface)
- `surface.h` (surface management)
- `buff.h` (buffer serialization)

## Design Patterns
- **Strategy Pattern**: Blitter/RLEBlitter interfaces allow runtime selection of blitting algorithms
- **Facade Pattern**: Hides complex blitting operations behind simple surface-surface interfaces
- **Not inferable**: Buffer serialization functions suggest potential use of **Memento Pattern** for surface state preservation

*Token count: 198*
