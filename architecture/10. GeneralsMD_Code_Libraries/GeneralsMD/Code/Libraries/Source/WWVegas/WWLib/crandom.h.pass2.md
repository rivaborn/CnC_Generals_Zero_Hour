# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crandom.h - Enhanced Analysis

## Architectural Role
This file provides the core random number generation utility used throughout the engine for both synchronized (game logic) and unsynchronized (visual/audio effects) operations. The `FreeRandom` global instance serves as a convenience for non-critical randomness, while the `CRandom` class itself is likely instantiated by subsystems requiring deterministic behavior.

## Cross-References
### Incoming
- Game logic systems (AI, unit behavior, mission scripts)
- Rendering effects (particle systems, animations)
- Audio systems (sound effect timing)
- Networking (potentially for desynchronized client-side effects)

### Outgoing
- `Random2Class` (underlying generator implementation)
- `wwdebug.h` (assertions for range validation)

## Design Patterns
- **Singleton-like Global**: `FreeRandom` provides a shared instance for unsynchronized randomness, avoiding repeated instantiation.
- **Wrapper/Adapter**: `CRandom` adapts the lower-level `Random2Class` to provide game-specific randomness APIs.
- **Inline Functions**: Performance-critical methods are inlined to reduce overhead in hot paths (e.g., particle effects).

*Not inferable*: No clear use of Factory, Observer, or other patterns from this header alone.
