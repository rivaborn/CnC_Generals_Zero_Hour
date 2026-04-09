# Generals/Code/Tools/ParticleEditor/ParticleEditorDialog.cpp - Enhanced Analysis

## Architectural Role
This file is the central UI controller for the particle system editor tool, bridging the MFC-based dialog system with the game's particle system runtime. It manages the editor's state, coordinates updates between UI controls and particle system data, and handles serialization of particle system definitions.

## Cross-References
### Incoming
- **ParticleEditorExport.h**: Uses `ParticlePriorityNames`, `EmissionVolumeTypeNames`, etc. for combo box initialization
- **GameClient/ParticleSys.h**: Interfaces with `ParticleSystem` class for runtime data
- **Sub-dialog classes** (`CColorAlphaDialog`, `CSwitchesDialog`, etc.): Hosts and delegates to these for specialized parameter editing

### Outgoing
- **MFC framework**: Extends `CDialog` and uses `CComboBox`, `CWnd` for UI rendering
- **Panel classes** (`EmissionPanelPoint`, `VelocityPanelOrtho`, etc.): Instantiates and manages these for type-specific editing
- **Particle system runtime**: Modifies `ParticleSystem` properties via `signalParticleSystemEdit`

## Design Patterns
- **Composite**: Manages a hierarchy of panel objects (`m_emissionTypePanels`, `m_velocityTypePanels`, etc.) that share a common interface
- **Observer**: UI controls notify the dialog of changes via message map handlers (e.g., `ON_EN_KILLFOCUS`), which then propagate to the particle system
- **State**: Uses boolean flags (`m_shouldReload`, `m_shouldWriteINI`) to track pending operations, deferring execution until the next update cycle
