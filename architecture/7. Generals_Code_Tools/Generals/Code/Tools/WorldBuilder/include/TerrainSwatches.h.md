# Generals/Code/Tools/WorldBuilder/include/TerrainSwatches.h

## Purpose
Header file for the `TerrainSwatches` class, a Windows UI component for rendering terrain textures in the WorldBuilder tool.

## Responsibilities
- Define the `TerrainSwatches` class inheriting from `CWnd`.
- Declare methods for rendering terrain textures (`OnPaint`, `DrawMyTexture`).
- Provide message map for Windows message handling.

## Key Types
- **TerrainSwatches (Class)**: A Windows child window for displaying terrain texture swatches.

## Key Functions
### TerrainSwatches::TerrainSwatches
- Purpose: Constructor for the `TerrainSwatches` class.
- Calls: None.

### TerrainSwatches::~TerrainSwatches
- Purpose: Destructor for the `TerrainSwatches` class.
- Calls: None.

### TerrainSwatches::OnPaint
- Purpose: Handles the WM_PAINT message to redraw the window.
- Calls: None (implementation not shown).

### TerrainSwatches::DrawMyTexture
- Purpose: Renders a texture onto the device context.
- Calls: None (implementation not shown).

### DECLARE_MESSAGE_MAP
- Purpose: Declares the message map for Windows message routing.
- Calls: None.

## Globals
- None.

## Dependencies
- `lib/BaseType.h` (for `Int`, `UnsignedByte` types).
- MFC (`CWnd`, `CDC`, `DECLARE_MESSAGE_MAP`, `afx_msg`).
- Windows SDK (for UI and graphics handling).
