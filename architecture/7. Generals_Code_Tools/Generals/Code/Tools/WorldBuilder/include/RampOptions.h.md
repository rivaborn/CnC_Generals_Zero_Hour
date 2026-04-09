# Generals/Code/Tools/WorldBuilder/include/RampOptions.h

## Purpose
Defines the `RampOptions` class for configuring ramp settings in the WorldBuilder tool.

## Responsibilities
- Manages ramp application toggle (`m_shouldApplyTheRamp`)
- Stores ramp width value (`m_rampWidth`)
- Handles UI events for ramp options
- Provides accessors for ramp state and width

## Key Types
- **RampOptions (Class)**: UI panel for ramp configuration.
- **(anonymous enum) (Enum)**: Contains `IDD` for dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### `RampOptions()`
- Purpose: Constructor for `RampOptions`.
- Calls: Not inferable.

### `~RampOptions()`
- Purpose: Destructor for `RampOptions`.
- Calls: Not inferable.

### `shouldApplyTheRamp()`
- Purpose: Returns whether ramps should be applied.
- Calls: Not inferable.

### `getRampWidth()`
- Purpose: Returns the current ramp width.
- Calls: Not inferable.

### `OnApply()`
- Purpose: Handles ramp application event.
- Calls: Not inferable.

### `OnWidthChange()`
- Purpose: Handles ramp width change event.
- Calls: Not inferable.

## Globals
- **TheRampOptions (RampOptions*)**: Global instance of `RampOptions`.

## Dependencies
- `OptionsPanel.h`: Base class for options panels.
- `Resource.h`: Contains dialog resource IDs.
- MFC (`CWnd`, `afx_msg`): UI framework dependencies.
