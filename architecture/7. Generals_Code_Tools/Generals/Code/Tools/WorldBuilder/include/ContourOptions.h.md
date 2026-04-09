# Generals/Code/Tools/WorldBuilder/include/ContourOptions.h

## Purpose
Defines a modeless dialog for configuring contour rendering options in WorldBuilder.

## Responsibilities
- Manages UI controls for contour step, offset, and width
- Provides static accessors for current contour settings
- Handles slider and button events for interactive updates

## Key Types
- **ContourOptions (Class)**: Modeless dialog for contour options
- **(anonymous enum)**: Defines min/max values for contour parameters
- **MIN_CONTOUR_STEP (Enum)**: Minimum contour step value (1)
- **MAX_CONTOUR_STEP (Enum)**: Maximum contour step value (10)
- **MIN_CONTOUR_OFFSET (Enum)**: Minimum contour offset value (-10)
- **MAX_CONTOUR_OFFSET (Enum)**: Maximum contour offset value (10)
- **MIN_WIDTH (Enum)**: Minimum contour width value (1)
- **MAX_WIDTH (Enum)**: Maximum contour width value (6)
- **(anonymous enum)**: Dialog resource ID (IDD_CONTOUR_OPTIONS)

## Key Functions
### ContourOptions()
- Purpose: Standard constructor for the dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles DDX/DDV data exchange for dialog controls
- Calls: None

### OnInitDialog()
- Purpose: Initializes dialog controls and values
- Calls: None

### OnHScroll()
- Purpose: Handles horizontal scroll events for sliders
- Calls: None

### OnShowContours()
- Purpose: Handles contour visibility toggle
- Calls: None

### getContourWidth()
- Purpose: Returns current contour width value
- Calls: None

### getContourOffset()
- Purpose: Returns current contour offset value
- Calls: None

### getContourStep()
- Purpose: Returns current contour step value
- Calls:
