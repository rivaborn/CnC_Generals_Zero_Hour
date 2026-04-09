# Generals/Code/Libraries/Source/WWVegas/WWLib/blitter.h - Enhanced Analysis

## Architectural Role
This file defines core abstraction interfaces for pixel manipulation, serving as a foundational layer in the rendering pipeline. It enables polymorphic blitting operations, critical for both standard and RLE-compressed texture handling in the W3D renderer.

## Cross-References
### Incoming
- Rendering subsystem (W3D) - uses `Blitter`/`RLEBlitter` for texture operations
- UI system - likely calls `Blitter` for surface manipulation
- Animation system - may use `RLEBlitter` for compressed sprite data

### Outgoing
- None (pure interface file)

## Design Patterns
- **Strategy Pattern**: Abstract `Blitter` classes allow runtime selection of blitting algorithms
- **Interface Segregation**: Separate `RLEBlitter` for compressed data specialization
- **Template Method**: `Blit()` wrapper implements overlap logic, delegates to pure virtual methods

*Not inferable*: Concrete implementations or usage patterns in calling subsystems.
