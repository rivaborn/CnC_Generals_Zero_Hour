# Generals/Code/Libraries/Source/WWVegas/WWLib/xmouse.h

## Purpose
Defines the abstract `Mouse` class for managing game mouse cursor behavior in the SAGE engine.

## Responsibilities
- Abstracts mouse cursor rendering and input handling
- Manages cursor visibility, capture/release, and coordinate conversion
- Supports custom cursor artwork with hotspot positioning
- Handles conditional hiding based on screen regions

## Key Types
- **Mouse (Class)**: Abstract base class for mouse cursor management
- **Surface (Class)**: Forward declaration for surface rendering
- **ShapeSet (Class)**: Forward declaration for cursor shape data

## Key Functions
### `Set_Cursor`
- Purpose: Sets the game-drawn mouse cursor imagery
- Calls: None

### `Hide_Mouse`
- Purpose: Hides the game-drawn mouse cursor
- Calls: None

### `Show_Mouse`
- Purpose: Shows the game-drawn mouse cursor
- Calls: None

### `Release_Mouse`
- Purpose: Releases mouse control to the OS
- Calls: None

### `Capture_Mouse`
- Purpose: Captures mouse control from the OS
- Calls: None

### `Is_Captured`
- Purpose: Checks if mouse is captured
- Calls: None

### `Conditional_Hide_Mouse`
- Purpose: Hides mouse if within specified region
- Calls: None

### `Conditional_Show_Mouse`
- Purpose: Shows mouse if previously hidden by region check
- Calls: None

### `Get_Mouse_State`
- Purpose: Returns mouse visibility state
- Calls: None

### `Get_Mouse_X`
- Purpose: Returns mouse X coordinate
- Calls: None

### `Get_Mouse_Y`
- Purpose: Returns mouse Y coordinate
- Calls: None

### `Set_Mouse_X
