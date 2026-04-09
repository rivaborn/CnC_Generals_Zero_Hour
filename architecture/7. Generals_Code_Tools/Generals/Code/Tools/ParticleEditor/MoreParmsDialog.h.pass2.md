# Generals/Code/Tools/ParticleEditor/MoreParmsDialog.h - Enhanced Analysis

## Architectural Role
This header defines a specialized MFC dialog class for the Particle Editor tool, bridging the gap between the UI layer and the particle system's parameter management. It encapsulates the logic for editing advanced particle parameters, serving as a tool-specific extension of the broader particle system framework.

## Cross-References
### Incoming
- Likely called by the main Particle Editor UI framework (e.g., `ParticleEditor.h`) to display the dialog.
- May be referenced by particle system serialization code to load/save additional parameters.

### Outgoing
- Interacts with the particle system core (e.g., `ParticleSystem.h`) via `performUpdate()`.
- Uses MFC base classes (`CDialog`, `CWnd`) for UI rendering and event handling.

## Design Patterns
- **Bridge Pattern**: Separates the abstraction (particle system parameters) from its implementation (UI controls).
- **Observer Pattern**: The dialog likely observes particle system changes to update the UI (`performUpdate` with `toUI=true`).
- **Template Method**: `performUpdate` acts as a template method for bidirectional synchronization between UI and data.
