# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/TunnelContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the tunnel containment system, a specialized variant of `OpenContain` that delegates storage and management to the player's `TunnelTracker`. It bridges the gap between individual tunnel objects and the global tunnel network, handling unit transit, healing, and network integrity during capture/destruction.

## Cross-References
### Incoming
- **AIUpdate**: Likely calls `update()` for per-frame processing
- **Object**: Calls containment methods during unit entry/exit
- **DamageSystem**: Invokes `harmAndForceExitAllContained` on tunnel destruction

### Outgoing
- **TunnelTracker**: Core dependency for all containment operations
- **OpenContain**: Base class for standard containment behavior
- **Player**: Accesses owning player for tunnel system retrieval

## Design Patterns
- **Delegation**: Delegates containment logic to `TunnelTracker` instead of managing its own list
- **Template Method**: Extends `OpenContain` with tunnel-specific behavior while preserving base functionality
- **Observer**: Notifies units via `onRemovedFrom` during containment changes (implied by event triggers)

*Not inferable*: Exact iterator handling strategy in `harmAndForceExitAllContained` (comment suggests crash fix but implementation unclear).
