# Generals/Code/Tools/WorldBuilder/include/WaterOptions.h

## Purpose
Defines the `WaterOptions` dialog class for the WorldBuilder tool, handling water height and polygon creation settings.

## Responsibilities
- Manages water height and spacing parameters
- Controls water polygon creation and river generation
- Handles UI updates and slider interactions
- Provides static accessors for water settings

## Key Types
- **WaterOptions (Class)**: Dialog for water editing options
- **WBPopupSliderButton (Class)**: Slider control for water height
- **MovePolygonUndoable (Class)**: Undoable action for polygon movement
- **PolygonTrigger (Class)**: Trigger for polygon-related actions
- **MapObject (Class)**: Base map object class
- **(anonymous enum) (Enum)**: Dialog resource ID

## Key Functions
### `DoDataExchange`
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: `CDataExchange` methods

### `OnInitDialog`
- Purpose: Initializes the dialog UI
- Calls: Not inferable

### `updateTheUI`
- Purpose: Updates the UI based on current settings
- Calls: Not inferable

### `updateHeight`
- Purpose: Updates the water height value
- Calls: Not inferable

### `adjustCount`
- Purpose: Adjusts the number of points in a polygon trigger
- Calls: Not inferable

### `GetPopSliderInfo`
- Purpose: Provides slider configuration for popup sliders
- Calls: Not inferable

### `PopSliderChanged`
- Purpose: Handles slider value changes
- Calls: Not inferable

### `PopSliderFinished`
- Purpose: Handles slider value finalization
- Calls: Not inferable

## Globals
- **m_staticThis (WaterOptions*)**: Reference to the floating panel instance
- **m_waterHeight
