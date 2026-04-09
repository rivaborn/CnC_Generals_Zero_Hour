# Generals/Code/Tools/ParticleEditor/ParticleEditorDialog.h

## Purpose
Header for the Particle Editor dialog class, managing particle system templates and their properties in the Generals game editor.

## Responsibilities
- Manages particle system templates and their properties
- Provides UI for editing particle system parameters
- Handles particle system selection and modification
- Coordinates with child dialog panels for specific parameter groups

## Key Types
- **RGBColorKeyframe (struct)**: Not inferable.
- **RandomKeyframe (struct)**: Not inferable.
- **SwitchType (enum)**: Defines particle system switch types (hollow, oneshot, align, emit above ground, particle upward).
- **DebugWindowDialog (class)**: Main particle editor dialog class handling particle system editing.

## Key Functions
### DebugWindowDialog::InitPanel
- Purpose: Initializes the particle editor panel.
- Calls: Not inferable.

### DebugWindowDialog::updateParticleAsciiStringParm
- Purpose: Updates a particle system's ASCII string parameter.
- Calls: Not inferable.

### DebugWindowDialog::getColorValueFromSystem
- Purpose: Retrieves color keyframe data from a particle system.
- Calls: Not inferable.

### DebugWindowDialog::updateColorValueToSystem
- Purpose: Updates color keyframe data in a particle system.
- Calls: Not inferable.

### DebugWindowDialog::performUpdate
- Purpose: Updates either the UI from the particle system or vice versa.
- Calls: Not inferable.

## Globals
- **ISwapablePanel (interface)**: Interface for swappable panels in the editor.

## Dependencies
- `<map>`, `<string>`, `<vector>`, `<list>` for STL containers
- `ParticleSys.h` for particle system definitions
- `CColorAlphaDialog.h`, `CSwitchesDialog.h`, `MoreParmsDialog.h` for child dialog panels
- `CDialog` base class from MFC
- Particle system template classes and enums
