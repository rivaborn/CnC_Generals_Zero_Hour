# Generals/Code/Tools/WorldBuilder/src/FeatherOptions.cpp

## Purpose
Handles the UI dialog for feathering options in WorldBuilder, managing brush tool parameters.

## Responsibilities
- Manages feather, rate, and radius sliders and edit controls
- Updates FeatherTool with new parameter values
- Handles UI initialization and message routing

## Key Types
- FeatherOptions (Class): Dialog for feathering tool options
- PopSliderButton (Class): Slider control helper (external)

## Key Functions
### setFeather
- Purpose: Updates feather value in UI and internal state
- Calls: None

### setRate
- Purpose: Updates rate value in UI and internal state
- Calls: None

### setRadius
- Purpose: Updates radius value in UI and internal state
- Calls: None

### OnInitDialog
- Purpose: Initializes dialog controls and sets default values
- Calls: setFeather, setRate, setRadius

### OnChangeSizeEdit
- Purpose: Handles manual edit box changes for feather size
- Calls: FeatherTool::setFeather

### GetPopSliderInfo
- Purpose: Provides slider configuration for specific controls
- Calls: None

### PopSliderChanged
- Purpose: Handles slider value changes and updates UI/state
- Calls: FeatherTool::setFeather, FeatherTool::setRadius, FeatherTool::setRate

## Globals
- m_staticThis (FeatherOptions*): Singleton instance pointer
- m_currentFeather (Int): Current feather size value
- m_currentRate (Int): Current rate value
- m_currentRadius (Int): Current radius value

## Dependencies
- MFC classes (CDialog, CWnd)
- FeatherTool class
- Resource IDs (IDC_SIZE_EDIT, IDC_RATE_EDIT, IDC_RADIUS_EDIT, etc.)
- Constants (MIN_FEATHER_SIZE, MAX_FEATHER_SIZE, etc.)
