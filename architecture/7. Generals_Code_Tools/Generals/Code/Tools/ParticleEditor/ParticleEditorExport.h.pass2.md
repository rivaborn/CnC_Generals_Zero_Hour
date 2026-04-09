# Generals/Code/Tools/ParticleEditor/ParticleEditorExport.h - Enhanced Analysis

## Architectural Role
This header defines the C-compatible interface for the Particle Editor tool, serving as the bridge between the editor's internal implementation and external tools (likely the game or build pipeline). It abstracts particle system management operations into a stable ABI.

## Cross-References
### Incoming
- Likely called by the game's asset build system or the editor's host application (e.g., `Generals/Code/Tools/ParticleEditor/ParticleEditor.cpp` or external tools).

### Outgoing
- Interacts with `ParticleSystemTemplate` (forward-declared) and likely internal editor state management (not exposed in header).

## Design Patterns
- **Facade Pattern**: Exposes a simplified C interface to hide complex particle system management logic.
- **Command Pattern**: Functions like `NextParticleEditorBehavior` suggest a command queue for editor operations.
- **Resource Management**: Explicit `Create`/`Destroy` pairs for dialog lifecycle management.
