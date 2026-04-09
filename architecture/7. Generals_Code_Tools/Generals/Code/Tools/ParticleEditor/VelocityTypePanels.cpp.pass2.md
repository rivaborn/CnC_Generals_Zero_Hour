# Generals/Code/Tools/ParticleEditor/VelocityTypePanels.cpp - Enhanced Analysis

## Architectural Role
This file implements UI panels for the Particle Editor tool, bridging MFC-based UI controls with the particle system's velocity parameter backend. It serves as a concrete example of the editor's modular panel architecture, where each velocity type (orthogonal, spherical, etc.) has its own panel class inheriting from `ISwapablePanel`.

## Cross-References
### Incoming
- `ParticleEditorDialog.cpp` (parent dialog) - calls `performUpdate` and `OnParticleSystemEdit` methods
- `ISwapablePanel` base class - provides panel management infrastructure

### Outgoing
- `DebugWindowDialog` (parent) - delegates parameter synchronization via `getVel*FromSystem`/`updateVel*ToSystem`
- MFC framework - for UI control management and message handling

## Design Patterns
- **Bridge Pattern**: Separates UI controls from particle system data via the parent dialog's synchronization methods
- **Template Method**: `performUpdate` uses a consistent pattern for all velocity types (read/write to UI)
- **Observer Pattern**: UI events trigger particle system updates through the parent dialog's signal mechanism

*Not inferable*: Specific particle system implementation details are abstracted behind parent dialog methods.
