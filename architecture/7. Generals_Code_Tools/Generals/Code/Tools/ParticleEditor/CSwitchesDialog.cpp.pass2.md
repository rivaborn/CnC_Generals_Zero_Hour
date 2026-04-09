# Generals/Code/Tools/ParticleEditor/CSwitchesDialog.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for particle system switch controls in the Particle Editor tool, bridging MFC dialog controls with the underlying particle system state. It acts as a specialized view/controller for particle system flags, delegating state management to the parent `DebugWindowDialog`.

## Cross-References
### Incoming
- `ParticleEditorDialog.h` (parent class includes this dialog)
- MFC framework (dialog message handlers)

### Outgoing
- `DebugWindowDialog` (parent dialog for particle system access)
- MFC controls (`CButton`, `CDialog`)

## Design Patterns
- **Observer Pattern**: Dialog notifies parent of changes via `signalParticleSystemEdit()`
- **Mediator Pattern**: Parent `DebugWindowDialog` mediates between UI and particle system
- **Data Transfer Object**: Switch states passed via simple `Bool` parameters

*Not inferable*: No clear use of Factory, Strategy, or Decorator patterns.
