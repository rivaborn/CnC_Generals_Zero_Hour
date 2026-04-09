# Generals/Code/Tools/ParticleEditor/ParticleTypePanels.h - Enhanced Analysis

## Architectural Role
This file defines the UI panel classes for the Particle Editor tool, which is part of the SAGE engine's content creation pipeline. These panels allow artists to edit particle system properties, bridging the gap between the runtime particle system and the editor's UI.

## Cross-References
### Incoming
- Likely called by the main Particle Editor window class (e.g., `ParticleEditorDoc` or similar) to create and manage these panels.
- May be referenced by the panel management system (e.g., `ISwapablePanel` factory or container).

### Outgoing
- Calls into `ISwapablePanel` base class methods for panel management.
- Interacts with the particle system runtime (e.g., `ParticleSystem` or `Particle` classes) during `performUpdate`.

## Design Patterns
- **Template Method**: `performUpdate` is a template method where subclasses implement the actual synchronization logic.
- **Inheritance Hierarchy**: `ParticlePanelStreak` inherits from `ParticlePanelParticle`, indicating shared behavior with extensions.
- **Resource-Based UI**: Uses resource IDs (`IDD`) to define dialog layouts, typical of MFC-based tools.
