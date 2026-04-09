# Generals/Code/Libraries/Source/WWVegas/WWLib/trackwin.h

## Purpose
Header file defining a `TrackWindow` class for managing sub-windows within a larger window, though currently disabled via `#ifdef NEVER`.

## Responsibilities
- Defines `TrackWindow` class for sub-window tracking (inactive).
- Provides methods for setting/resetting sub-window dimensions.
- Offers getters for sub-window and full-window properties.
- Uses `Rect` for window dimension storage.

## Key Types
- `TrackWindow` (Class): Tracks sub-window dimensions within a larger window.
- `Rect` (Struct): Used for storing window dimensions (external).

## Key Functions
### `TrackWindow(int width, int height)`
- Purpose: Constructor initializing sub-window and full-window dimensions.
- Calls: None.

### `Set(Rect const & rect)`
- Purpose: Updates the sub-window dimensions and full-window if unset.
- Calls: None.

### `Reset(void)`
- Purpose: Resets sub-window to full-window dimensions.
- Calls: `Full_Rect()`.

### `Get_X()`, `Get_Y()`, `Get_Width()`, `Get_Height()`
- Purpose: Getters for sub-window dimensions.
- Calls: None.

### `Full_Width()`, `Full_Height()`
- Purpose: Getters for full-window dimensions.
- Calls: None.

## Globals
- None.

## Dependencies
- `trect.h` (included, but unused due to `#ifdef NEVER`).
- `Rect` (assumed from `trect.h`).
