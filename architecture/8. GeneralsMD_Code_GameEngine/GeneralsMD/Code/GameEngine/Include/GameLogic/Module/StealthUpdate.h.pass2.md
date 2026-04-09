# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StealthUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the stealth system's core logic, bridging game object behavior with rendering and AI. It manages stealth states, disguise mechanics, and detection logic, acting as a middleware between object status updates and visual/audio feedback systems.

## Cross-References
### Incoming
- **AI/Pathfinding**: Likely queries `calcStealthedStatusForPlayer` for target visibility
- **Rendering (W3D)**: Uses `isDisguised()` and `getFriendlyOpacity()` for visual effects
- **Networking**: `receiveGrant()` may sync stealth state across clients
- **UI**: `EvaMessage` events trigger in-game notifications

### Outgoing
- **Object Status System**: Checks `m_requiredStatus`/`m_forbiddenStatus` masks
- **FX System**: Applies `m_disguiseFX`/`m_disguiseRevealFX` via `FXList`
- **Weapon System**: `m_requiresWeaponSetType` ties stealth to weapon states
- **Player/Team Logic**: `m_disguiseAsPlayerIndex` interacts with team systems

## Design Patterns
- **Strategy Pattern**: Stealth behavior varies by `m_stealthLevel` (attacking/moving/etc.)
- **State Pattern**: `m_enabled`, `m_disguised`, and transition flags manage stealth states
- **Observer Pattern**: `EvaMessage` events notify other systems of stealth changes

*Not inferable*: Exact implementation of `calcSleepTime()` or `hintDetectableWhileUnstealthed()`.
