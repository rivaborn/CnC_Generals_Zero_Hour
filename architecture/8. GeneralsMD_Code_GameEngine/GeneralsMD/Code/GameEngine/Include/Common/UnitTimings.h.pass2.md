# GeneralsMD/Code/GameEngine/Include/Common/UnitTimings.h - Enhanced Analysis

## Architectural Role
This header serves as a compile-time configuration point for unit timing diagnostics, allowing developers to toggle performance measurement features without modifying core game logic. It bridges the gap between debugging tools and runtime performance analysis.

## Cross-References
### Incoming
- Likely referenced by unit behavior files (`Unit.cpp`, `BehaviorTree.cpp`) and performance profiling tools
- May be included by timing-related utility classes in the `Common` subsystem

### Outgoing
- No direct outgoing references (pure header with preprocessor directive)

## Design Patterns
- **Feature Toggle Pattern**: Uses preprocessor defines to conditionally compile timing-related code
- **Header Guard Pattern**: Standard include protection to prevent multiple inclusions
- **Configuration Header Pattern**: Centralized location for build-time configuration options

*Not inferable*: No runtime patterns observable from this file alone.
