# Generals/Code/Tools/WorldBuilder/src/ObjectPreview.cpp

## Purpose
Handles rendering and displaying previews of game objects in the WorldBuilder tool.

## Responsibilities
- Renders 3D object previews using Direct3D
- Captures and converts render targets to bitmap data
- Displays previews in a Windows control
- Manages message handling for the preview window

## Key Types
- `ObjectPreview` (Class): Main preview control class
- `ThingTemplate` (Pointer): Reference to the object template being previewed

## Key Functions
### `saveSurface`
- Purpose: Captures a Direct3D surface to a BGRA pixel array
- Calls: `DX8Wrapper::_Get_D3D_Device8()`, `DX8Wrapper::Create_Render_Target()`, `DX8Wrapper::Set_Render_Target()`

### `generatePreview`
- Purpose: Generates a preview image for a given ThingTemplate
- Calls: `WbView3d::getBestModelName()`, `W3DAssetManager::Create_Render_Obj()`, `WW3D::Begin_Render()`, `WW3D::Render()`, `WW3D::End_Render()`

### `ObjectPreview::OnPaint`
- Purpose: Handles paint messages to render the preview
- Calls: `generatePreview()`, `DrawMyTexture()`

### `ObjectPreview::DrawMyTexture`
- Purpose: Draws the preview bitmap to the device context
- Calls: `::StretchDIBits()`

## Globals
- `SWATCH_OFFSET` (const int): Preview offset constant
- `PREVIEW_WIDTH`/`PREVIEW_HEIGHT` (const int): Preview dimensions

## Dependencies
- Direct3D 8 interfaces (`IDirect3DSurface8`)
- WW3D rendering system
- ThingTemplate/ThingFactory systems
- Windows GDI for bitmap rendering
- DX8Wrapper for device management
