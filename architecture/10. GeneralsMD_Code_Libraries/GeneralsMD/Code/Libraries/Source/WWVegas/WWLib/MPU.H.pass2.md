# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/MPU.H - Enhanced Analysis

## Architectural Role
This header provides low-level CPU performance measurement utilities, likely used by the engine's timing and profiling systems to optimize rendering and game logic performance.

## Cross-References
### Incoming
- Likely called by timing/performance monitoring systems (e.g., `GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Time.H`)

### Outgoing
- None (header-only, no direct dependencies)

## Design Patterns
- **Facade Pattern**: Exposes simple CPU measurement functions, hiding RDTSC instruction complexity
- **Utility Library**: Pure header with no state, providing reusable CPU metrics
- **Not inferable**: No other patterns clearly visible

*(Token count: 150)*
