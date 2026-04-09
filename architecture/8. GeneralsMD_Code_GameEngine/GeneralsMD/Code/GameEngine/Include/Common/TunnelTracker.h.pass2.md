# GeneralsMD/Code/GameEngine/Include/Common/TunnelTracker.h - Enhanced Analysis

## Architectural Role
This file defines the `TunnelTracker` class, which acts as a central manager for tunnel-related gameplay mechanics. It bridges the gap between tunnel objects (like caves) and the contained units, handling state synchronization, healing, and nemesis targeting across the network.

## Cross-References
### Incoming
- **Tunnel objects** (e.g., caves) call `onTunnelCreated`/`onTunnelDestroyed` to register/deregister.
- **Player logic** uses `iterateContained` to access tunnel contents for AI decisions.
- **Healing systems** invoke `healObjects` during tunnel-based regeneration.

### Outgoing
- **ContainModule** interface is mirrored for consistency with module-based containment.
- **Snapshot/Xfer** for serialization/deserialization during save/load.
- **Object callbacks** (`destroyObject`, `healObject`) for contained unit management.

## Design Patterns
- **Observer Pattern**: Tunnel objects notify `TunnelTracker` of lifecycle events.
- **Composite Pattern**: Manages a collection of contained objects with uniform operations.
- **State Caching**: Tracks nemesis targets with timestamps for time-limited behavior.
