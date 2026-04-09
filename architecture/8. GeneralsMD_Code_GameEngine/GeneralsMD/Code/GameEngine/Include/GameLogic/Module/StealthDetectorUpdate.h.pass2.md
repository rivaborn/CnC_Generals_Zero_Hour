# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StealthDetectorUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the stealth detection system's core logic module, bridging game object behavior with the update framework. It handles detection mechanics, audio/visual feedback, and configuration parsing for stealth-related gameplay.

## Cross-References
### Incoming
- **GameObject/Thing subclasses**: Use this module for stealth detection (e.g., Radar Van, Observer)
- **UpdateManager**: Calls `update()` during game loop processing
- **AudioSystem**: Triggered by `m_pingSound`/`m_loudPingSound` events
- **ParticleSystem**: Uses templates for visual detection indicators

### Outgoing
- **UpdateModule base class**: Inherits core update behavior
- **MultiIniFieldParse**: For configuration data parsing
- **Thing methods**: Accesses object state (garrisoned/transported status)
- **KindOfSystem**: Evaluates target detection filters

## Design Patterns
- **Module Pattern**: Encapsulates stealth detection as a reusable component
- **Configuration Driven**: Uses `StealthDetectorUpdateModuleData` for externalized settings
- **Observer**: Notifies via audio/particles when detection occurs (implicit)
