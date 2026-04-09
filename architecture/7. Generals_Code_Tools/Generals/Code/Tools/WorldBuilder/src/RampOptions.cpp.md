# Generals/Code/Tools/WorldBuilder/src/RampOptions.cpp

## Purpose
Handles ramp configuration options in the WorldBuilder tool, including width settings and apply functionality.

## Responsibilities
- Manages ramp width input and validation
- Controls the "Apply" button behavior for ramp changes
- Maintains a singleton instance via `TheRampOptions`
- Handles UI event responses for ramp options panel

## Key Types
- `RampOptions` (Class): Dialog panel for ramp configuration
- `COptionsPanel` (Class): Base class for options dialogs

## Key Functions
### `RampOptions::RampOptions`
- Purpose: Constructor initializing ramp width and singleton instance
- Calls: None

### `RampOptions::~RampOptions`
- Purpose: Destructor cleaning up singleton reference
- Calls: None

### `RampOptions::shouldApplyTheRamp`
- Purpose: Checks and resets the apply flag for ramp changes
- Calls: None

### `RampOptions::OnApply`
- Purpose: Sets the apply flag when user clicks Apply
- Calls: None

### `RampOptions::OnWidthChange`
- Purpose: Updates ramp width from UI input
- Calls: `GetDlgItem`, `GetWindowText`, `atof`

## Globals
- `TheRampOptions` (RampOptions*): Singleton instance of the ramp options panel

## Dependencies
- `StdAfx.h`, `RampOptions.h`
- `CWnd`, `CString`, `COptionsPanel`, `Bool` (MFC/Windows types)
- `BEGIN_MESSAGE_MAP`, `ON_BN_CLICKED`, `ON_EN_CHANGE` (MFC macros)
