# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DMouse.h

## Purpose
Defines the W3DMouse class, extending Win32Mouse to handle cursor rendering using W3D (Westwood 3D) methods.

## Responsibilities
- Manage mouse cursor display via W3D rendering
- Handle different cursor types (D3D textures, W3D models, polygons)
- Control cursor animation and hotspot positioning
- Initialize and clean up cursor assets

## Key Types
- W3DMouse (Class): Mouse interface using W3D for cursor rendering
- CameraClass (Class): Reference to cursor camera (forward declared)
- SurfaceClass (Class): Reference to cursor surface textures (forward declared)

## Key Functions
### W3DMouse::init
- Purpose: Initialize mouse system and assets
- Calls: initD3DAssets, initW3DAssets, initPolygonAssets

### W3DMouse::setCursor
- Purpose: Set the current mouse cursor type
- Calls: setCursorDirection, loadD3DCursorTextures

### W3DMouse::draw
- Purpose: Render the current cursor
- Calls: Not inferable (implementation in .cpp)

### W3DMouse::initD3DAssets
- Purpose: Load D3D texture assets for cursors
- Calls: Not inferable

### W3DMouse::initW3DAssets
- Purpose: Load W3D model assets for cursors
- Calls: Not inferable

### W3DMouse::initPolygonAssets
- Purpose: Load polygon assets for cursors
- Calls: Not inferable

## Globals
None

## Dependencies
- Win32Mouse.h (inheritance)
- Forward declarations: CameraClass, SurfaceClass
