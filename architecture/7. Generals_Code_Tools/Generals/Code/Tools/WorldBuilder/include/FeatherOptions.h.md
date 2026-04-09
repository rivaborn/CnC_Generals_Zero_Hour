# Generals/Code/Tools/WorldBuilder/include/FeatherOptions.h

## Purpose
Defines a modeless dialog for configuring brush feathering options in the WorldBuilder tool.

## Responsibilities
- Manages UI controls for feather size, smoothing rate, and radius
- Provides static methods to update feathering parameters
- Implements popup slider functionality for parameter adjustment
- Handles data exchange between UI and internal state

## Key Types
- **FeatherOptions (Class)**: Modeless dialog for feathering options
- **(anonymous enum)**: Defines min/max values for feather size, rate, and radius
- **MIN_FEATHER_SIZE (Enum)**: Minimum feather size value (2)
- **MAX_FEATHER_SIZE (Enum)**: Maximum feather size value (51)
- **MIN_RATE (Enum)**: Minimum smoothing rate value (1)
- **MAX_RATE (Enum)**: Maximum smoothing rate value (10)
- **MIN_RADIUS (Enum)**: Minimum smoothing radius value (1)
- **MAX_RADIUS (Enum)**: Maximum smoothing radius value (5)
- **(anonymous enum)**: Dialog resource ID definition

## Key Functions
### DoDataExchange
- Purpose: Handles data exchange between UI controls and member variables
- Calls: Not inferable

### OnInitDialog
- Purpose: Initializes the dialog controls
- Calls: Not inferable

### OnChangeSizeEdit
- Purpose: Handles changes to the size edit control
- Calls: Not inferable

### setFeather
- Purpose: Updates the current feather size value
- Calls: Not inferable

### setRate
- Purpose: Updates the current smoothing rate value
- Calls: Not inferable

### setRadius
- Purpose: Updates the current smoothing radius value
- Calls: Not inferable

### GetPopSliderInfo
- Purpose: Provides slider configuration information
- Calls: Not
