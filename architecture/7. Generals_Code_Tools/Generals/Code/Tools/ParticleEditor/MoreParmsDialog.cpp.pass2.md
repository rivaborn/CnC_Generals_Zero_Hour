# Generals/Code/Tools/ParticleEditor/MoreParmsDialog.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for advanced particle system parameters in the Particle Editor tool, bridging MFC dialog controls with the underlying particle system data model. It serves as a specialized panel within the larger Particle Editor framework, handling user input and visualization of particle behavior parameters.

## Cross-References
### Incoming
- `ParticleEditorDialog.h` (parent class interface)
- MFC framework classes (`CDialog`, `CComboBox`, `CWnd`)

### Outgoing
- Calls into `DebugWindowDialog` (parent) for particle system data access
- Uses `ParticleSystemInfo` enum for wind motion types

## Design Patterns
- **Observer Pattern**: Dialog notifies parent via `signalParticleSystemEdit()` when parameters change
- **Mediator Pattern**: Parent `DebugWindowDialog` acts as mediator between UI and particle system data
- **Template Method**: `performUpdate()` uses a consistent pattern for all parameter sync operations

*Not inferable*: No clear use of Factory, Strategy, or Decorator patterns in this file.
