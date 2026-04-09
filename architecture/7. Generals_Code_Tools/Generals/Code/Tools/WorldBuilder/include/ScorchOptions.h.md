# Generals/Code/Tools/WorldBuilder/include/ScorchOptions.h

## Purpose
Defines the `ScorchOptions` dialog class for configuring scorch effects in WorldBuilder.

## Responsibilities
- Manages UI for scorch effect settings (type, size, radius)
- Handles user input for scorch modifications
- Updates selected map objects with new scorch parameters
- Provides popup slider functionality for radius adjustment

## Key Types
- **ScorchOptions (Class)**: Dialog for scorch effect configuration
- **MapObject (Class)**: Reference to map objects being modified
- **(anonymous enum) (Enum)**: Dialog resource ID
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### ScorchOptions::updateTheUI
- Purpose: Refreshes the UI with current scorch settings
- Calls: Not inferable

### ScorchOptions::changeSize
- Purpose: Applies new scorch size to selected objects
- Calls: Not inferable

### ScorchOptions::changeScorch
- Purpose: Applies new scorch type to selected objects
- Calls: Not inferable

### ScorchOptions::getAllSelectedDicts
- Purpose: Collects property dictionaries of selected objects
- Calls: Not inferable

### ScorchOptions::update
- Purpose: Static method to trigger UI update
- Calls: updateTheUI

### ScorchOptions::GetPopSliderInfo
- Purpose: Provides slider configuration for radius popup
- Calls: Not inferable

### ScorchOptions::PopSliderChanged
- Purpose: Handles real-time slider value changes
- Calls: Not inferable

### ScorchOptions::PopSliderFinished
- Purpose: Applies final slider value after user release
- Calls: Not inferable

## Globals
- **m_scorchtype (Scorches)**: Current scorch effect type
