# Generals/Code/Tools/ParticleEditor/EmissionTypePanels.cpp

## Purpose
Implements UI panels for editing different particle emission types (point, line, box, sphere, cylinder) in the Particle Editor tool.

## Responsibilities
- Manages UI panels for each emission type
- Synchronizes UI controls with particle system parameters
- Handles user input for emission shape parameters
- Triggers particle system updates when values change

## Key Types
- **EmissionPanelPoint (class)**: Panel for point emission type
- **EmissionPanelLine (class)**: Panel for line emission type
- **EmissionPanelBox (class)**: Panel for box emission type
- **EmissionPanelSphere (class)**: Panel for sphere emission type
- **EmissionPanelCylinder (class)**: Panel for cylinder emission type

## Key Functions
### performUpdate
- Purpose: Synchronizes UI controls with particle system parameters or vice versa
- Calls: `GetDlgItem`, `GetParent`, `getLineFromSystem`, `updateLineToSystem`, `getHalfSizeFromSystem`, `updateHalfSizeToSystem`, `getCylinderRadiusFromSystem`, `updateCylinderRadiusToSystem`, `getCylinderLengthFromSystem`, `updateCylinderLengthToSystem`

### OnParticleSystemEdit
- Purpose: Notifies parent dialog that particle system needs updating
- Calls: `GetParent`, `signalParticleSystemEdit`

## Globals
- **ARBITRARY_BUFF_SIZE (const int)**: Buffer size for text conversion (128)

## Dependencies
- `StdAfx.h`
- `EmissionTypePanels.h`
- `ParticleEditorDialog.h`
- `ISwapablePanel` (base class)
- `DebugWindowDialog` (parent class)
- MFC UI classes (`CWnd`, `BEGIN_MESSAGE_MAP`, etc.)
