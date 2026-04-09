# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DMouse.h

## Purpose
Defines the W3DMouse class, extending Win32Mouse to handle cursor rendering using W3D (Westwood 3D) methods.

## Responsibilities
- Manage mouse cursor display via W3D rendering
- Handle cursor animations and hotspots
- Load/unload cursor assets (textures, models, polygons)
- Support multiple cursor drawing modes (D3D, W3D, polygon)

## Key Types
- **W3DMouse (Class)**: Mouse interface using W3D for cursor rendering
- **CameraClass (Class)**: Forward reference to camera handling
- **SurfaceClass (Class)**: Forward reference to surface handling

## Key Functions
### W3DMouse::init
- Purpose: Initialize mouse system
- Calls: Not inferable

### W3DMouse::setCursor
- Purpose: Set the current mouse cursor
- Calls: Not inferable

### W3DMouse::draw
- Purpose: Render the cursor
- Calls: Not inferable

### W3DMouse::initD3DAssets
- Purpose: Load D3D textures for mouse cursors
- Calls: Not inferable

### W3DMouse::initW3DAssets
- Purpose: Load W3D models for mouse cursors
- Calls: Not inferable

### W3DMouse::initPolygonAssets
- Purpose: Load polygon images for cursor rendering
- Calls: Not inferable

## Globals
- None

## Dependencies
- Win32Mouse.h (inheritance)
- Forward references: CameraClass, SurfaceClass
