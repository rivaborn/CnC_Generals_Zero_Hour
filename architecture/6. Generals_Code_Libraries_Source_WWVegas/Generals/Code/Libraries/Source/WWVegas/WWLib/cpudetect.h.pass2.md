# Generals/Code/Libraries/Source/WWVegas/WWLib/cpudetect.h - Enhanced Analysis

## Architectural Role
This header defines the CPU detection subsystem, providing runtime hardware capability queries used by performance-critical components like the renderer and game logic. It serves as the engine's hardware abstraction layer for CPU features, cache configuration, and memory topology.

## Cross-References
### Incoming
- Rendering pipeline (W3D) for feature detection (SSE/SSE2/MMX)
- Game logic for timing/performance optimization
- Audio subsystem for CPU load balancing
- Memory manager for cache-aware allocations

### Outgoing
- Direct hardware access via CPUID instruction
- Platform-specific memory queries (Windows/Unix)
- String utilities for log generation

## Design Patterns
- **Singleton-like access**: Static methods with internal state management
- **Factory pattern**: CPU type detection with manufacturer-specific initialization
- **Adapter pattern**: Wraps raw CPUID results into structured enums and flags

*Not inferable: Exact initialization sequence or thread-safety guarantees.*
