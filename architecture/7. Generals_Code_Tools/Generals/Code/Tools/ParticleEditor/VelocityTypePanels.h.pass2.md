# Generals/Code/Tools/ParticleEditor/VelocityTypePanels.h - Enhanced Analysis

## Architectural Role
This file defines specialized UI panels for the Particle Editor tool, extending the `ISwapablePanel` interface to handle different particle velocity types. It bridges the gap between the particle system's data model and the editor's UI, enabling real-time synchronization.

## Cross-References
### Incoming
- **ParticleEditorMain**: Likely instantiates and manages these panels, calling `InitPanel` and `performUpdate` during editor workflow.
- **ParticleSystem**: The core particle system calls into these panels' `OnParticleSystemEdit` handlers when particle data changes.

### Outgoing
- **ISwapablePanel**: Inherits base functionality for panel management.
- **MFC Framework**: Uses `CWnd`, message maps, and dialog resources for UI rendering and event handling.

## Design Patterns
- **Strategy Pattern**: Each velocity panel implements a different strategy for velocity type editing, allowing the editor to switch between them dynamically.
- **Observer Pattern**: Panels observe the particle system and update the UI (`performUpdate(toUI=true)`), while also notifying the system of UI changes (`performUpdate(toUI=false)`).
- **Template Method**: `performUpdate` abstracts the synchronization logic, with subclasses implementing type-specific behavior.
