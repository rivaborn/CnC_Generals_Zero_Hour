# Generals/Code/Tools/ParticleEditor/CSwitchesDialog.h - Enhanced Analysis

## Architectural Role
This file defines a dialog class for the Particle Editor tool, which is part of the game's content creation pipeline. It bridges the UI layer with the particle system data model, enabling artists to tweak particle effects in real-time.

## Cross-References
### Incoming
- Likely called by other Particle Editor dialogs or the main editor window to manage switch editing UI
- May be instantiated by the DebugWindowDialog (parent class) to handle particle system configuration

### Outgoing
- Calls into particle system data structures (not shown in header) to sync UI state
- Uses MFC framework classes (CDialog, CWnd) for UI rendering and event handling

## Design Patterns
- **Observer Pattern**: `performUpdate()` suggests bidirectional synchronization between UI and particle system data
- **MVC (Model-View-Controller)**: Separates particle system data (model) from UI presentation (view) with controller logic in this dialog
- **Dependency Injection**: Parent DebugWindowDialog is injected via constructor for context access

*Not inferable*: No other patterns clearly visible from header alone.
