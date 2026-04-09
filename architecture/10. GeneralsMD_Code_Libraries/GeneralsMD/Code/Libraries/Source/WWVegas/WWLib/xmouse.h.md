# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/xmouse.h

## Purpose
Defines the abstract `Mouse` class for managing game-drawn mouse cursors in the SAGE engine.

## Responsibilities
- Provides interface for mouse cursor management (visibility, position, shape).
- Supports mouse capture/release for OS interaction.
- Handles mouse rendering on surfaces.
- Manages coordinate conversion between OS and game spaces.

## Key Types
- **Mouse (Class)**: Abstract base class for mouse cursor management.
- **Surface (Class)**: Forward declaration for surface rendering.
- **ShapeSet (Class)**: Forward declaration for cursor shapes.

## Key Functions
### `Set_Cursor`
- Purpose: Sets the mouse cursor artwork and hotspot.
- Calls: None (pure virtual).

### `Hide_Mouse`
- Purpose: Hides the game-drawn mouse cursor.
- Calls: None (pure virtual).

### `Capture_Mouse`
- Purpose: Takes control of the mouse from the OS.
- Calls: None (pure virtual).

### `Get_Mouse_State`
- Purpose: Returns the mouse visibility state.
- Calls: None (pure virtual).

### `Draw_Mouse`
- Purpose: Renders the mouse cursor on a surface.
- Calls: None (pure virtual).

### `Convert_Coordinate`
- Purpose: Converts OS screen coordinates to game coordinates.
- Calls: None (pure virtual).

## Globals
- None.

## Dependencies
- `trect.h` (for `Rect` type).
- Forward declarations: `Surface`, `ShapeSet`.
