# Generals/Code/Tools/ParticleEditor/MoreParmsDialog.h

## Purpose
Header for a dialog class used in the Particle Editor tool to manage additional particle system parameters.

## Responsibilities
- Define the `MoreParmsDialog` class inheriting from `CDialog`.
- Declare methods for initializing the dialog and updating UI/particle system.
- Handle particle system parameter editing events.

## Key Types
- **MoreParmsDialog (Class)**: Dialog for editing additional particle system parameters.
- **(anonymous enum) (Enum)**: Contains the dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### MoreParmsDialog()
- Purpose: Constructor for the dialog.
- Calls: None.

### ~MoreParmsDialog()
- Purpose: Destructor for the dialog.
- Calls: None.

### InitPanel()
- Purpose: Initialize the dialog panel.
- Calls: None.

### performUpdate()
- Purpose: Update either the UI from the particle system or vice versa.
- Calls: None.

### OnParticleSystemEdit()
- Purpose: Handle particle system edit events.
- Calls: None.

## Globals
- None.

## Dependencies
- `resource.h`: For dialog resource definitions.
- `Lib/BaseType.h`: For basic type definitions.
- `CDialog`: Base MFC dialog class.
- `CWnd`: MFC window class.
- `DECLARE_MESSAGE_MAP()`: MFC macro for message map declaration.
