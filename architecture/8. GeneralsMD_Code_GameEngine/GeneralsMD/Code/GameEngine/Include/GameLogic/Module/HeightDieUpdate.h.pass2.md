# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HeightDieUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a specialized update module for the SAGE engine's entity component system, handling height-based destruction logic. It integrates with the game's physics and terrain systems to manage object lifecycle based on vertical position.

## Cross-References
### Incoming
- Game object initialization code (likely in `Thing` or `Object` classes)
- Module factory system (via `MAKE_STANDARD_MODULE_MACRO`)
- Configuration parsing system (via `MultiIniFieldParse`)

### Outgoing
- Terrain height query system (for `m_targetHeightAboveTerrain` logic)
- Particle system management (for `m_destroyAttachedParticlesAtHeight`)
- Game time/frame tracking (for `m_initialDelay` and `m_earliestDeathFrame`)

## Design Patterns
- **Component Pattern**: Implements as an update module in the SAGE ECS
- **State Tracking**: Uses flags (`m_hasDied`, `m_particlesDestroyed`) for one-time operations
- **Configuration Driven**: Uses `buildFieldParse` for data-driven behavior setup

*Not inferable: Exact terrain/particle system integration points*
