# Generals/Code/Tools/ParticleEditor/ParticleEditor.h - Enhanced Analysis

## Architectural Role
This header defines the core MFC application class for the Particle Editor tool, serving as the entry point for the debug window DLL. It bridges the tool's UI with the broader engine's particle system, enabling runtime visualization and editing of particle effects.

## Cross-References
### Incoming
- Likely called by the Particle Editor's main DLL initialization code and the dialog implementation (`DebugWindowDialog`).

### Outgoing
- Relies on MFC framework (`CWinApp`) and the forward-declared `DebugWindowDialog` class for UI management.

## Design Patterns
- **Singleton-like behavior**: The `CDebugWindowApp` instance manages the single `DebugWindowDialog` via getter/setter, suggesting a centralized access point for the tool's UI.
- **MFC Document-View separation**: Uses MFC's `CWinApp` base class, adhering to the framework's architectural patterns for Windows applications.
- **Forward declaration**: Uses `DebugWindowDialog` forward declaration to decouple this header from the dialog's implementation details.
