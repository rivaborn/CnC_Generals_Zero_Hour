# Generals/Code/Tools/ParticleEditor/ParticleEditor.cpp - Enhanced Analysis

## Architectural Role
This file serves as the bridge between the game engine and the particle editor tool, exposing a DLL interface for particle system management. It encapsulates MFC-based UI logic while providing a clean abstraction for the game to interact with the editor.

## Cross-References
### Incoming
- Game engine tools (e.g., debug console) call exported functions like `CreateParticleSystemDialog`, `DestroyParticleSystemDialog`, and `NextParticleEditorBehavior` to control the editor.

### Outgoing
- Calls into `ParticleEditorDialog.h` for UI operations (e.g., `DebugWindowDialog::updateCurrentParticleSystem`).
- Relies on MFC framework (`CWinApp`, `CDialog`) for window management.

## Design Patterns
- **Facade Pattern**: Exposes simplified methods (e.g., `AppendParticleSystem`) to hide MFC complexity.
- **Singleton Pattern**: Uses `theApp` as a global instance to manage the editor state.
- **State Query Pattern**: Functions like `ShouldWriteINI` return boolean flags to drive editor behavior (used in `NextParticleEditorBehavior`).

**Not inferable**: No clear use of Observer or Command patterns despite UI interactions.
