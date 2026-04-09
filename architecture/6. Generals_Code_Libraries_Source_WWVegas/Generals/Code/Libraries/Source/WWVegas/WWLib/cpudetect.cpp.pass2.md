# Generals/Code/Libraries/Source/WWVegas/WWLib/cpudetect.cpp - Enhanced Analysis

## Architectural Role
This file serves as the engine's hardware/OS abstraction layer, providing runtime system characterization for performance optimization and compatibility checks. Its data is consumed by subsystems like the renderer (W3D) for feature detection and the audio system for CPU load balancing.

## Cross-References
### Incoming
- **W3D Renderer**: Uses CPU feature flags (SSE/SSE2/MMX) for shader/path selection
- **Audio System**: Checks CPU speed for dynamic mixing buffer sizing
- **Game Logic**: Queries OS version for compatibility warnings (e.g., Windows 98 workarounds)
- **Networking**: Uses processor speed for bandwidth estimation

### Outgoing
- **System Timer (systimer.h)**: For RDTSC-based speed measurement
- **Threading (thread.h)**: For CPU core count detection (implied by MPU usage)
- **Debug System (wwdebug.h)**: For logging hardware/OS details

## Design Patterns
- **Singleton**: CPUDetectInitClass ensures one-time initialization
- **Registry**: Windows9xVersionTable acts as a lookup table for OS detection
- **Inline Assembly**: Direct CPUID/RDTSC usage for low-level hardware access

*Not inferable*: Exact usage patterns of FeatureBits/ExtendedFeatureBits by other subsystems.
