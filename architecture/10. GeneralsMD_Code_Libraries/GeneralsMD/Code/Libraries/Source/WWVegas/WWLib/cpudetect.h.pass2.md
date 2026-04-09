# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/cpudetect.h - Enhanced Analysis

## Architectural Role
This header defines the CPU detection subsystem, providing runtime hardware capability queries used by the SAGE engine's performance optimization layer. It serves as the foundation for feature-based code paths in rendering, physics, and AI systems.

## Cross-References
### Incoming
- Rendering subsystem (uses SSE/SSE2 detection)
- Physics simulation (queries CPU features)
- Memory management (uses cache/memory stats)
- Audio subsystem (checks MMX/3DNow support)

### Outgoing
- Direct hardware access (CPUID instruction)
- OS-specific memory queries (via platform abstraction)

## Design Patterns
- **Singleton-like access**: Static methods with internal state management
- **Feature flag pattern**: Boolean flags for CPU capabilities
- **Platform abstraction**: Conditional compilation for Windows/Unix memory types

Rules followed. Output under 400 tokens.
