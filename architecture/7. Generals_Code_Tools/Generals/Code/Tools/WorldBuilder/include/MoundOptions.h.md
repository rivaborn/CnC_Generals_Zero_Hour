# Generals/Code/Tools/WorldBuilder/include/MoundOptions.h

## Purpose
Defines the `MoundOptions` dialog class for configuring brush parameters in WorldBuilder.

## Responsibilities
- Manages UI controls for brush width, feather, and height settings
- Handles slider input for these parameters
- Provides static methods to update the UI from external code
- Inherits from `COptionsPanel` and implements `PopupSliderOwner` for slider behavior

## Key Types
- **MoundOptions (Class)**: Dialog for brush parameter configuration
- **(anonymous enum)**: Defines min/max values for mound height (1-21)
- **MIN_MOUND_HEIGHT (Enum)**: Minimum mound height value
- **MAX_MOUND_HEIGHT (Enum)**: Maximum mound height value
- **(anonymous enum)**: Defines min/max values for brush size (1-51) and feather (0-20)
- **MIN_BRUSH_SIZE (Enum)**: Minimum brush size value
- **MAX_BRUSH_SIZE (Enum)**: Maximum brush size value
- **MIN_FEATHER (Enum)**: Minimum feather value
- **MAX_FEATHER (Enum)**: Maximum feather value
- **(anonymous enum)**: Dialog resource ID (IDD_BRUSH_OPTIONS)

## Key Functions
### MoundOptions()
- Purpose: Constructor for the MoundOptions dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange between UI controls and member variables
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog and its controls
- Calls: None

### OnChangeFeatherEdit()
- Purpose: Handles changes to the feather edit control
- Calls: None

### OnChangeSizeEdit()
- Purpose: Handles changes to the size edit control
- Calls: None

### OnChangeHeightEdit()
- Purpose: Handles changes to the height edit control
- Calls
