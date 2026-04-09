# Generals/Code/Tools/WorldBuilder/include/ShadowOptions.h

## Purpose
Header file for the ShadowOptions dialog class used in WorldBuilder to configure shadow rendering settings.

## Responsibilities
- Define the ShadowOptions dialog class
- Declare shadow color and intensity properties
- Declare event handlers for UI controls
- Declare message map for MFC dialog

## Key Types
- ShadowOptions (Class): MFC dialog for shadow configuration
- (anonymous enum) (Enum): Contains IDD_SHADOW_OPTIONS dialog ID
- IDD (Enum): Dialog resource identifier

## Key Functions
### ShadowOptions::DoDataExchange
- Purpose: Handle data exchange between dialog controls and member variables
- Calls: Not inferable

### ShadowOptions::setShadowColor
- Purpose: Update shadow color based on current RGB values
- Calls: Not inferable

### ShadowOptions::OnChangeAlphaEdit
- Purpose: Handle changes to alpha/transparency control
- Calls: Not inferable

### ShadowOptions::OnChangeBaEdit
- Purpose: Handle changes to blue channel control
- Calls: Not inferable

### ShadowOptions::OnChangeGaEdit
- Purpose: Handle changes to green channel control
- Calls: Not inferable

### ShadowOptions::OnChangeRaEdit
- Purpose: Handle changes to red channel control
- Calls: Not inferable

### ShadowOptions::OnInitDialog
- Purpose: Initialize dialog controls
- Calls: Not inferable

## Globals
- None

## Dependencies
- CDialog (MFC base class)
- CDataExchange (MFC data exchange)
- Real (floating-point type)
- MFC message map macros (DECLARE_MESSAGE_MAP, afx_msg)
- Dialog resource ID (IDD_SHADOW_OPTIONS)
