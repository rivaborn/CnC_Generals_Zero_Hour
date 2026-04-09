# Generals/Code/Libraries/Source/WWVegas/WW3D2/statistics.h - Enhanced Analysis

## Architectural Role
This header defines the core interface for the SAGE engine's rendering performance monitoring system, bridging the rendering pipeline (WW3D2) with debugging tools. It provides frame-level metrics critical for both in-engine diagnostics and external profiling tools.

## Cross-References
### Incoming
- Rendering pipeline components (e.g., `TextureClass`, `ShaderClass` implementations)
- Debug UI systems (for displaying statistics overlays)
- External profiling tools (via exposed metrics)

### Outgoing
- Directly interacts with:
  - Texture management subsystem (for `TextureClass` tracking)
  - Shader system (for `ShaderClass` metrics)
  - Frame timing system (via `Begin_Statistics`/`End_Statistics` lifecycle)

## Design Patterns
- **Facade Pattern**: Exposes a simplified interface to complex rendering metrics, hiding implementation details.
- **Singleton-like Behavior**: Implicit single instance of statistics tracker (no constructor/destructor visible).
- **Macro-Based Instrumentation**: Uses preprocessor macros (`DX8_RECORD_*`) for low-overhead metric collection points.

*Not inferable*: No clear Observer pattern (metrics appear push-based rather than event-driven).
