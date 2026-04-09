# Generals/Code/Tools/ParticleEditor/ParticleTypePanels.cpp - Enhanced Analysis

## Architectural Role
This file implements UI panels for the Particle Editor tool, bridging MFC-based UI controls with the particle system backend. It handles texture and drawable object selection, demonstrating the tool's role in content creation workflows.

## Cross-References
### Incoming
- `ParticleEditorDialog.h` (parent dialog class)
- MFC framework (`CWnd`, `CComboBox`, `CFileFind`)

### Outgoing
- `DebugWindowDialog` (parent class for system updates)
- Filesystem operations via `_tfinddata_t`

## Design Patterns
- **Template Method**: `performUpdate` defines synchronization logic while subclasses override specific behavior.
- **Observer**: Combo box selection changes trigger system updates via message map.
- **Composite**: `ParticlePanelStreak` inherits from `ParticlePanelParticle`, reusing texture selection logic.

*Not inferable*: Exact relationship with W3D rendering system or networking.
