# Generals/Code/Tools/ParticleEditor/ShaderTypePanels.cpp - Enhanced Analysis

## Architectural Role
This file is part of the Particle Editor tooling suite, specifically handling the UI panels for shader type configuration. It bridges the gap between the W3D rendering pipeline and the editor's UI, allowing artists to tweak shader parameters without direct code access.

## Cross-References
### Incoming
- Likely called by the main Particle Editor UI framework (e.g., `ParticleEditor.cpp`) when shader panels are instantiated or updated.
- May be referenced by shader serialization/deserialization logic in the toolchain.

### Outgoing
- Calls into the W3D shader system (e.g., `W3DShader.h`) for shader parameter validation and preview rendering.
- Depends on the Particle Editor's UI framework (e.g., `UIPanel.h`) for panel management and event handling.

## Design Patterns
- **Mediator**: Acts as a mediator between the UI and the underlying shader system, encapsulating interaction logic.
- **Factory Method**: Likely uses factory methods to create shader-specific panels based on type (inferred from filename and tool context).
- **Observer**: Panels probably register as observers for shader parameter changes, updating the UI dynamically.
