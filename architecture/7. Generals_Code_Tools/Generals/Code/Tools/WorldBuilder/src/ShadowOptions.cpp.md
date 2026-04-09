# Generals/Code/Tools/WorldBuilder/src/ShadowOptions.cpp

## Purpose
Handles shadow color configuration in the WorldBuilder tool.

## Responsibilities
- Manages shadow color dialog UI
- Updates shadow color based on user input
- Converts between color formats (float and integer)
- Initializes dialog with current shadow settings

## Key Types
- ShadowOptions (Class): Dialog for shadow color configuration

## Key Functions
### setShadowColor
- Purpose: Applies current color settings to the shadow manager
- Calls: TheW3DShadowManager->setShadowColor

### OnChangeAlphaEdit/OnChangeBaEdit/OnChangeGaEdit/OnChangeRaEdit
- Purpose: Handles edit control changes for alpha, blue, green, and red channels respectively
- Calls: setShadowColor

### OnInitDialog
- Purpose: Initializes dialog controls with current shadow color values
- Calls: TheW3DShadowManager->getShadowColor

## Globals
- None

## Dependencies
- "stdafx.h", "worldbuilder.h", "Lib\BaseType.h", "rendobj.h", "common/GlobalData.h", "ShadowOptions.h", "W3DDevice/GameClient/W3DShadow.h"
- CDialog, CWnd, CString, DEBUG_LOG, TheW3DShadowManager
