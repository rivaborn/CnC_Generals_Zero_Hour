# Generals/Code/Tools/ParticleEditor/CSwitchesDialog.h

## Purpose
Defines a dialog class for editing particle system switches in the Particle Editor tool.

## Responsibilities
- Manages UI for particle system switch editing
- Synchronizes UI with particle system data
- Provides access to parent debug window
- Handles particle system edit events

## Key Types
- CSwitchesDialog (Class): Dialog for editing particle system switches
- DebugWindowDialog (Class): Parent debug window (forward declared)
- (anonymous enum) (Enum): Contains IDD constant for dialog resource ID

## Key Functions
### CSwitchesDialog()
- Purpose: Constructor for CSwitchesDialog.
- Calls: None

### InitPanel()
- Purpose: Initializes the dialog panel.
- Calls: None

### performUpdate()
- Purpose: Updates either UI from particle system or vice versa.
- Calls: None

### GetDWDParent()
- Purpose: Returns parent DebugWindowDialog pointer.
- Calls: None

### OnParticleSystemEdit()
- Purpose: Handles particle system edit events.
- Calls: None

## Globals
- None

## Dependencies
- "Lib/BaseType.h" (for Bool type)
- CDialog (MFC base class)
- CWnd (MFC base class)
- IDD_PSEd_EditSwitchesDialog (resource ID, defined elsewhere)
