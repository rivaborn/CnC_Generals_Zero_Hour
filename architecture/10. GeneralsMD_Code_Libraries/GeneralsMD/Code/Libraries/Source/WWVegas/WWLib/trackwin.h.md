# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/trackwin.h

## Purpose
Header file defining a `TrackWindow` class for managing sub-windows within a larger window.

## Responsibilities
- Tracks sub-window dimensions and position.
- Provides methods to set, reset, and query window data.
- Maintains full window dimensions for clipping and reset operations.

## Key Types
- TrackWindow (Class): Manages sub-window tracking within a larger window.

## Key Functions
### TrackWindow(int width, int height)
- Purpose: Constructor initializing sub-window and full-window dimensions.
- Calls: None.

### Set(Rect const & rect)
- Purpose: Sets the sub-window dimensions and updates full-window if not already set.
- Calls: None.

### Reset(void)
- Purpose: Resets the sub-window to full dimensions.
- Calls: None.

### Get_X(), Get_Y(), Get_Width(), Get_Height(), Get_Rect()
- Purpose: Query sub-window dimensions and position.
- Calls: None.

### Full_Width(), Full_Height(), Full_Rect()
- Purpose: Query full-window dimensions.
- Calls: None.

## Globals
- None.

## Dependencies
- `trect.h` (included conditionally under `NEVER`).
- `Rect` (struct/class used but not defined here).
