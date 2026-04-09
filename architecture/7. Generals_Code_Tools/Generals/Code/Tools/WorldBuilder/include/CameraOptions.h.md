# Generals/Code/Tools/WorldBuilder/include/CameraOptions.h

## Purpose
Header for the CameraOptions dialog class in WorldBuilder, managing camera settings and UI interactions.

## Responsibilities
- Manages camera pitch and movement controls
- Handles UI data exchange and updates
- Implements popup slider functionality for camera adjustments
- Provides camera reset and value application logic

## Key Types
- **CameraOptions (Class)**: Dialog for camera settings in WorldBuilder
- **(anonymous enum) (Enum)**: Contains IDD_CAMERA_OPTIONS dialog identifier
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### CameraOptions()
- Purpose: Constructor for CameraOptions dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles DDX/DDV data exchange for dialog controls
- Calls: None

### OnCameraReset()
- Purpose: Resets camera to default position
- Calls: Not inferable

### OnMove()
- Purpose: Handles window movement events
- Calls: Not inferable

### OnInitDialog()
- Purpose: Initializes dialog controls and values
- Calls: Not inferable

### OnChangePitchEdit()
- Purpose: Handles changes to pitch edit control
- Calls: Not inferable

### OnShowWindow()
- Purpose: Handles window show/hide events
- Calls: Not inferable

### GetPopSliderInfo()
- Purpose: Provides popup slider configuration
- Calls: None

### PopSliderChanged()
- Purpose: Handles popup slider value changes
- Calls: None

### PopSliderFinished()
- Purpose: Handles popup slider completion
- Calls: None

### update()
- Purpose: Updates camera settings from UI controls
- Calls: Not inferable

## Globals
- **CAMERA_OPTIONS_PANEL_SECTION (String)**: Section name for configuration

## Dependencies
- CDialog
