# Generals/Code/Tools/ParticleEditor/EmissionTypePanels.h - Enhanced Analysis

## Architectural Role
This file defines specialized UI panels for particle emission types in the Particle Editor tool, extending the `ISwapablePanel` base class. It bridges the gap between the particle system's data model and the editor's UI, enabling real-time synchronization and parameter editing.

## Cross-References
### Incoming
- Likely called by the main Particle Editor UI framework to instantiate and manage these panels
- `ISwapablePanel` users (e.g., panel management system) would interact with these classes

### Outgoing
- Calls into `ISwapablePanel` base class methods
- Interacts with MFC UI framework (CWnd, dialog resources)
- Synchronizes with particle system data (via `performUpdate`)

## Design Patterns
- **Template Method**: `performUpdate` defines a common interface for UI synchronization, with implementation varying per emission type
- **Strategy**: Each panel class encapsulates behavior for a specific emission type, allowing runtime selection
- **Observer**: Panels react to particle system edits (via `OnParticleSystemEdit`), suggesting a loose coupling with the system's state
