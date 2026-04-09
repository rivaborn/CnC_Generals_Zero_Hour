# Generals/Code/Tools/WorldBuilder/src/GlobalLightOptions.cpp

## Purpose
Handles global lighting options in the WorldBuilder tool, allowing users to adjust light properties for terrain and objects.

## Responsibilities
- Manages UI for light angle, color, and intensity controls
- Updates lighting parameters in real-time
- Handles light feedback visualization in 3D view
- Resets lighting to default values
- Persists panel position in config

## Key Types
- **GlobalLightOptions (class)**: Main dialog class for lighting controls
- **Vector3 (struct)**: 3D vector for light direction calculations
- **RGBColor (struct)**: Color representation for lighting

## Key Functions
### calcNewLight
- Purpose: Calculates new light direction vector from angle inputs
- Calls: Vector3::Set, Vector3::Rotate_X/Y/Z, WWMath::Sin/Cos

### SpitLights
- Purpose: Logs current lighting settings for debugging
- Calls: DEBUG_LOG

### GlobalLightOptions::applyAngle
- Purpose: Applies angle changes to light direction and updates UI
- Calls: WbView3d::setLighting, WbView3d::doLightFeedback

### GlobalLightOptions::applyColor
- Purpose: Updates light color properties from UI inputs
- Calls: WbView3d::setLighting

## Globals
- **TheGlobalData (GlobalData**)**: Access to global lighting data
- **TheWritableGlobalData (GlobalData**)**: Access to writable lighting data

## Dependencies
- "stdafx.h", "resource.h", "Lib\BaseType.h", "GlobalLightOptions.h", "WorldBuilderDoc.h", "common/GlobalData.h", "WbView3D.h"
- CDialog, CWnd, CString, CColorDialog, WWMath, DEBUG_LOG, DEBUG_CRASH
- Global constants: K_SUN, K_ACCENT1, K_ACCENT2, K_TERRAIN, K_OBJECTS, K_BOTH
