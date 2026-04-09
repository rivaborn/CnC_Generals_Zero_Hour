# Generals/Code/Tools/WorldBuilder/include/ImpassableOptions.h

## Purpose
Defines a dialog class for configuring impassable slope options in the WorldBuilder tool.

## Responsibilities
- Manages slope angle settings for impassable terrain
- Validates slope values within [0,90] degree range
- Provides UI for previewing impassable areas
- Handles dialog initialization and message routing

## Key Types
- **ImpassableOptions (Class)**: Dialog for slope configuration
- **(anonymous enum) (Enum)**: Contains IDD constant
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### ImpassableOptions()
- Purpose: Constructor initializing slope values
- Calls: None

### ~ImpassableOptions()
- Purpose: Destructor
- Calls: None

### ValidateSlope()
- Purpose: Validates and clamps slope values
- Calls: None

### OnInitDialog()
- Purpose: Initializes dialog controls
- Calls: None

### OnAngleChange()
- Purpose: Handles slope angle change events
- Calls: None

### OnPreview()
- Purpose: Handles preview button click
- Calls: None

## Globals
- None

## Dependencies
- CDialog (MFC class)
- Real (floating-point type)
- Bool (boolean type)
- DECLARE_MESSAGE_MAP() (MFC macro)
- IDD_IMPASSABLEOPTIONS (resource ID)
