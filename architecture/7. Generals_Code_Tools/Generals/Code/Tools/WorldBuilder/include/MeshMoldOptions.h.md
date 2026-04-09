# Generals/Code/Tools/WorldBuilder/include/MeshMoldOptions.h

## Purpose
Header file for the MeshMoldOptions dialog class used in WorldBuilder for mesh molding operations.

## Responsibilities
- Manages mesh molding parameters (angle, height, scale)
- Handles UI interactions for mesh molding
- Provides preview and apply functionality
- Implements popup slider controls for parameter adjustment

## Key Types
- **MeshMoldOptions (Class)**: Dialog for mesh molding options
- **(anonymous enum)**: Defines min/max values for angle, height, and scale
- **MIN_ANGLE/MAX_ANGLE/MIN_HEIGHT/MAX_HEIGHT/MIN_SCALE/MAX_SCALE (Enum values)**: Parameter limits
- **(anonymous enum)**: Contains IDD dialog identifier
- **IDD (Enum value)**: Dialog resource ID

## Key Functions
### MeshMoldOptions()
- Purpose: Constructor for MeshMoldOptions dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### OnInitDialog()
- Purpose: Initializes the dialog
- Calls: Not inferable

### OnPreview()
- Purpose: Handles preview functionality
- Calls: Not inferable

### OnApplyMesh()
- Purpose: Applies mesh molding changes
- Calls: Not inferable

### GetPopSliderInfo()
- Purpose: Provides slider configuration information
- Calls: Not inferable

### PopSliderChanged()
- Purpose: Handles slider value changes
- Calls: Not inferable

### PopSliderFinished()
- Purpose: Handles slider value finalization
- Calls: Not inferable

## Globals
- **m_currentHeight (Real)**: Current height value
- **m_currentScale (Real)**: Current scale value
- **m_currentAngle (Int)**: Current angle value
- **m
