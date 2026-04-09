# Generals/Code/Tools/ParticleEditor/ParticleEditorDialog.h - Enhanced Analysis

## Architectural Role
This file defines the core UI controller for the particle editor tool, bridging the MFC-based dialog system with the game's particle system runtime data. It acts as a facade for particle system templates, exposing editor-specific accessors/mutators while isolating the underlying particle system implementation from direct UI manipulation.

## Cross-References
### Incoming
- Child dialog panels (`CColorAlphaDialog`, `CSwitchesDialog`, `MoreParmsDialog`) call methods like `getColorValueFromSystem` and `updateColorValueToSystem` to synchronize UI state with particle system data.
- The main editor framework likely instantiates `DebugWindowDialog` and handles its lifecycle events (e.g., `OnCreate`, `OnClose`).

### Outgoing
- Directly manipulates `ParticleSystemTemplate` instances via pointer (`m_particleSystem`), bypassing the game's normal particle system management.
- Uses `ISwapablePanel` interface to dynamically switch between different parameter editing panels (emission/velocity/particle types).

## Design Patterns
- **Facade Pattern**: Encapsulates complex particle system data access behind a simplified UI-oriented interface.
- **Observer Pattern**: The dialog monitors particle system changes (e.g., `OnParticleSystemChange`) to update the UI, though the concrete notification mechanism isn't visible here.
- **Strategy Pattern**: The `ISwapablePanel` array suggests different editing strategies for particle properties (emission/velocity/particle types) can be swapped at runtime.
