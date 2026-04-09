# Generals/Code/Tools/matchbot/global.h - Enhanced Analysis

## Architectural Role
This header defines the core global utilities for the matchbot tool, serving as the central access point for configuration, random number generation, and log management. It bridges the tool's runtime environment with the SAGE engine's configuration and threading subsystems.

## Cross-References
### Incoming
- Likely called by matchbot's main execution loop and other tool components needing configuration or RNG access
- Log rotation functions may be invoked by the tool's periodic maintenance or shutdown logic

### Outgoing
- Uses `ConfigFile` for configuration parsing (from engine's common utilities)
- Leverages `RandClass` for random number generation (engine-wide utility)
- Depends on `CritSec` and `ThreadFac` for thread-safe operations (engine's threading infrastructure)

## Design Patterns
- **Singleton**: `GlobalClass` provides a single global instance (`Global`) for shared state
- **Dependency Injection**: External types (`ConfigFile`, `RandClass`) are composed rather than inherited
- **Facade**: Hides complexity of configuration and log management behind simple interfaces

(Word count: 150)
