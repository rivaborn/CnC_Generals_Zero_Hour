# Generals/Code/GameEngine/Source/GameClient/Drawable/Update/BeaconClientUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the client-side behavior for beacon objects in the SAGE engine, bridging the rendering system (via Drawable) and the radar system. It handles visual effects (particle systems) and radar pulse events, with configuration driven by INI files and network synchronization via Xfer.

## Cross-References
### Incoming
- **GameClient/Drawable.h**: Uses `Drawable` for visual representation and state management.
- **GameClient/ParticleSys.h**: Relies on `ParticleSystem` for visual effects tied to beacons.
- **Common/Radar.h**: Triggers radar events (`RADAR_EVENT_BEACON_PULSE`) during updates.

### Outgoing
- **GameClient/Module/BeaconClientUpdate.h**: Defines the module's interface and data structures.
- **Common/Xfer.h**: Handles serialization/deserialization for network sync.
- **GameLogic/GameLogic.h**: Accesses game time (`TheGameLogic->getFrame()`) for timing logic.

## Design Patterns
- **Module Pattern**: Extends `ClientUpdateModule` to encapsulate beacon-specific behavior, promoting modularity in the update system.
- **Factory Method**: `createParticleSystem` dynamically creates particle systems based on object properties (e.g., `getIndicatorColor()`), allowing runtime customization.
- **Observer Pattern**: Implicitly participates by triggering radar events (`TheRadar->createEvent`), notifying the radar system of beacon pulses.
