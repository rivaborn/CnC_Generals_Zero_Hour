# Generals/Code/Tools/WorldBuilder/src/CameraOptions.cpp

## Purpose
Handles camera settings UI in WorldBuilder, allowing users to adjust camera pitch, zoom, and position.

## Responsibilities
- Manages camera parameter input/output via UI controls
- Updates camera settings in the 3D view
- Persists dialog position in app settings
- Handles popup sliders for camera pitch adjustment

## Key Types
- **CameraOptions (class)**: Dialog for camera settings
- **PopSliderButton (class)**: Slider control for pitch adjustment

## Key Functions
### OnCameraReset
- Purpose: Resets camera to default position
- Calls: `WbView3d::setDefaultCamera`, `update`

### OnMove
- Purpose: Saves dialog position when moved
- Calls: `AfxGetApp()->WriteProfileInt`

### stuffValuesIntoFields
- Purpose: Updates UI fields with current camera values
- Calls: `WbView3d::getCameraPitch`, `getHeightAboveGround`, `getCameraSource`, `getCameraTarget`

### applyCameraPitch
- Purpose: Applies new pitch value to camera
- Calls: `WbView3d::setCameraPitch`

### GetPopSliderInfo
- Purpose: Provides slider configuration for pitch control
- Calls: `WbView3d::getCameraPitch`

### PopSliderChanged
- Purpose: Updates pitch edit field when slider moves
- Calls: `putReal`

### OnChangePitchEdit
- Purpose: Applies new pitch when edit field changes
- Calls: `applyCameraPitch`

## Globals
- **m_updating (bool)**: Prevents recursive updates during UI changes

## Dependencies
- `WbView3d.h`, `WorldBuilderDoc.h`, MFC dialog classes
- `TheGlobalData` (external), `DEBUG_CRASH` macro
