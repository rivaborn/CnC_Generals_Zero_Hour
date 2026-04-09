# Generals/Code/Tools/ParticleEditor/CParticleEditorPage.h - Enhanced Analysis

## Architectural Role
This file defines the base UI class for the particle editor tool, part of the SAGE engine's toolchain. It bridges the MFC dialog framework with particle system editing functionality, likely used by level designers or modders to create/configure particle effects.

## Cross-References
### Incoming
- Toolchain UI controllers (e.g., main particle editor window) instantiate and manage this dialog
- Particle system serialization code may call `InitPanel()` to load/save templates

### Outgoing
- Relies on MFC's `CDialog` and `CWnd` for UI rendering and message handling
- Likely interacts with particle system runtime classes (e.g., `CParticleSystem`) during `InitPanel()`

## Design Patterns
- **Template Method**: `OnCreate()` suggests a hook for derived classes to customize dialog initialization
- **Observer**: Implicit via MFC message map for UI event handling (e.g., button clicks)
- **Composite**: Dialog contains child controls (not shown here, but implied by MFC structure)
