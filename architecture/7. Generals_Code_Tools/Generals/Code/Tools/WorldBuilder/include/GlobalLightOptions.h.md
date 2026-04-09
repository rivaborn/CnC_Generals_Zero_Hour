# Generals/Code/Tools/WorldBuilder/include/GlobalLightOptions.h

## Purpose
Defines the `GlobalLightOptions` dialog class for managing global lighting settings in WorldBuilder.

## Responsibilities
- Provides UI for adjusting light angles (azimuth/elevation) and colors
- Manages three light types: sun, accent1, and accent2
- Handles terrain/object lighting scope selection
- Implements popup sliders for precise value input
- Applies lighting changes to the scene

## Key Types
- **GlobalLightOptions (Class)**: Modeless dialog for global lighting controls
- **K_TERRAIN/K_OBJECTS/K_BOTH (Enum)**: Lighting scope targets
- **K_SUN/K_ACCENT1/K_ACCENT2 (Enum)**: Light types
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### `applyAngle(Int lightIndex=0)`
- Purpose: Applies the current angle settings to a light
- Calls: Not inferable

### `applyColor(Int lightIndex=0)`
- Purpose: Applies the current color settings to a light
- Calls: Not inferable

### `showLightFeedback(Int lightIndex=0)`
- Purpose: Updates visual feedback for light changes
- Calls: Not inferable

### `GetPopSliderInfo(const long sliderID, long *pMin, long *pMax, long *pLineSize, long *pInitial)`
- Purpose: Provides slider configuration for popup controls
- Calls: Not inferable

### `PopSliderChanged(const long sliderID, long theVal)`
- Purpose: Handles real-time slider value changes
- Calls: Not inferable

### `PopSliderFinished(const long sliderID, long theVal)`
- Purpose: Processes finalized slider values
- Calls: Not inferable

## Globals
- **kUIRedIDs/kUIGreen
