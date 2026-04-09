# Generals/Code/Tools/ParticleEditor/CColorAlphaDialog.h - Enhanced Analysis

## Architectural Role
This file defines the UI layer for particle system color/alpha editing in the Particle Editor tool, bridging MFC dialogs with the particle system's data model. It's part of the toolchain infrastructure, not the runtime engine.

## Cross-References
### Incoming
- Likely called by other Particle Editor dialogs (e.g., main editor window) to manage color/alpha properties
- May be referenced in tool project files (e.g., .dsp) for resource linking

### Outgoing
- Uses `CButtonShowColor` for color display/selection
- Interfaces with `ParticleSys` for data synchronization
- Relies on MFC (`CDialog`, `CWnd`) for UI framework

## Design Patterns
- **Observer Pattern**: Dialog reacts to color button events (`OnColor1`-`OnColor8`) to update state
- **Mediator Pattern**: Coordinates between UI controls (`m_colorButton`) and particle system data
- **Not inferable**: No clear use of Factory, Strategy, or Visitor patterns

*Token count: 198*
