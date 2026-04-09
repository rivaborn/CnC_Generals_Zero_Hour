# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/cpudetect.cpp - Enhanced Analysis

## Architectural Role
This file serves as the engine's hardware/OS abstraction layer, providing runtime system characterization for performance optimization and feature detection. Its data is consumed by rendering, physics, and AI subsystems to make CPU/GPU capability decisions.

## Cross-References
### Incoming
- **Rendering (W3D)**: Uses CPU feature flags (SSE/MMX) for shader selection
- **Physics/Simulation**: Relies on CPU speed metrics for timing calculations
- **AI**: Uses cache size data for memory access pattern optimization
- **Audio**: Checks CPU capabilities for mixing workload distribution

### Outgoing
- **System Timer (systimer.h)**: For CPU speed measurement via TIMEGETTIME()
- **Threading (thread.h)**: For safe RDTSC execution in multi-threaded context
- **Debug (wwdebug.h)**: For logging system information
- **Windows API**: Directly queries OS version and memory stats

## Design Patterns
- **Singleton Pattern**: CPUDetectInitClass ensures one-time initialization
- **Lookup Table Pattern**: Windows9xVersionTable for OS version identification
- **Feature Flag Pattern**: Boolean flags (HasSSESupport, etc.) for capability checking

*Not inferable: Exact usage patterns by consumers (e.g., conditional SSE code paths).*
