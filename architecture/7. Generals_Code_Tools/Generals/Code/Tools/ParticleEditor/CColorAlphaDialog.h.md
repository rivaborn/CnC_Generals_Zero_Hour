# Generals/Code/Tools/ParticleEditor/CColorAlphaDialog.h

## Purpose
Defines a dialog class for editing color and alpha properties of particle systems in the Particle Editor tool.

## Responsibilities
- Manages a dialog with color buttons and custom color array
- Handles color selection and updates between UI and particle system
- Initializes and synchronizes the dialog panel
- Provides event handlers for color button clicks

## Key Types
- **CColorAlphaDialog (Class)**: Dialog for editing particle system colors and alpha
- **CButtonShowColor (Class)**: Button control that displays a color
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### CColorAlphaDialog()
- Purpose: Constructor for the dialog
- Calls: None

### InitPanel()
- Purpose: Initializes the dialog panel
- Calls: None

### performUpdate()
- Purpose: Synchronizes data between UI and particle system
- Calls: None

### OnInitDialog()
- Purpose: Handles dialog initialization
- Calls: None

### OnColor1() - OnColor8()
- Purpose: Event handlers for color button clicks
- Calls: onColorPress()

### OnParticleSystemEdit()
- Purpose: Handles particle system edit events
- Calls: None

## Globals
- **m_customColors (DWORD[16])**: Stores custom color values
- **m_colorButton (CButtonShowColor[MAX_KEYFRAMES])**: Array of color buttons

## Dependencies
- CButtonShowColor.h
- GameClient/ParticleSys.h
- CDialog (MFC)
- afx_msg (MFC message map macros)
