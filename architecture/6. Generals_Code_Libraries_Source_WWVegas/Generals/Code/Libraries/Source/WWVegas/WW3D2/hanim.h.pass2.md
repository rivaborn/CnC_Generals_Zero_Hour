# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanim.h - Enhanced Analysis

## Architectural Role
This file defines the core animation abstraction layer for the W3D rendering pipeline, serving as the interface between animation data and the skeletal hierarchy system. It enables runtime animation blending and pivot-specific weight control, critical for character and vehicle animations in the game.

## Cross-References
### Incoming
- `hmorphanim.h` (uses `HAnimClass` as base for morph animations)
- Animation playback systems (call `Get_Transform`, `Get_Orientation`)
- Asset loading pipeline (uses `HAnimComboClass` for blended animations)

### Outgoing
- `quat.h`, `refcount.h` (for core math and memory management)
- `HTreeClass` (for skeletal hierarchy access in `NamedPivotMapClass`)
- `DynamicVectorClass` (for animation combo storage)

## Design Patterns
- **Strategy Pattern**: `HAnimClass` defines a virtual interface for different animation formats (raw, morph, etc.)
- **Composite Pattern**: `HAnimComboClass` aggregates multiple `HAnimComboDataClass` objects for blending
- **Proxy Pattern**: `Peek_` vs `Get_` methods manage reference counting transparently

*Not inferable*: Exact implementation of `Get_Transform` optimization (e.g., matrix caching).
