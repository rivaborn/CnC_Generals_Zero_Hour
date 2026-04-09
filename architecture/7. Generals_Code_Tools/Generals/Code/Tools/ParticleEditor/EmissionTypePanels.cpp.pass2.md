# Generals/Code/Tools/ParticleEditor/EmissionTypePanels.cpp - Enhanced Analysis

## Architectural Role
This file implements specialized UI panels for particle emission shape editing within the Particle Editor tool, extending the `ISwapablePanel` base class. It bridges the gap between the particle system's internal parameters and the editor's UI, enabling real-time parameter manipulation.

## Cross-References
### Incoming
- **ParticleEditorDialog.h**: Parent dialog class that handles particle system updates and provides data access methods.
- **ISwapablePanel**: Base class for panel swapping functionality in the editor UI.

### Outgoing
- **ParticleEditorDialog**: Calls methods like `signalParticleSystemEdit()`, `getLineFromSystem()`, and `updateLineToSystem()` to synchronize UI with particle system state.
- **MFC Framework**: Uses `CWnd`, `BEGIN_MESSAGE_MAP`, and dialog controls for UI rendering and event handling.

## Design Patterns
- **Bridge Pattern**: Decouples abstraction (particle emission types) from implementation (UI panels) via `ISwapablePanel`.
- **Observer Pattern**: Panels notify the parent dialog (`DebugWindowDialog`) of changes via `OnParticleSystemEdit`, triggering updates.
- **Template Method**: `performUpdate` uses a boolean flag (`toUI`) to control data flow direction (UI â System), enforcing a consistent update pattern.
