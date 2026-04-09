# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DSmudge.cpp

## Purpose
Implements the smudge system for rendering temporary visual effects (e.g., scorch marks) on the game world.

## Responsibilities
- Manages smudge rendering using Direct3D 8
- Tests hardware support for smudge effects
- Handles vertex/index buffers for smudge rendering
- Copies screen regions for smudge application
- Integrates with the W3D rendering pipeline

## Key Types
- `W3DSmudgeManager` (Class): Main smudge manager class
- `Smudge` (Struct): Represents individual smudge effects
- `SmudgeSet` (Class): Manages collections of smudges

## Key Functions
### `copyRect`
- Purpose: Copies a rectangular region from the render target to a buffer
- Calls: Direct3D device operations (GetRenderTarget, CreateImageSurface, CopyRects, LockRect)

### `testHardwareSupport`
- Purpose: Tests if the hardware supports smudge rendering
- Calls: Direct3D device operations, shader setup, and render state management

### `render`
- Purpose: Renders all active smudges in the scene
- Calls: Vertex/index buffer setup, shader configuration, and Direct3D draw calls

## Globals
- `TheSmudgeManager` (SmudgeManager*): Global instance of the smudge manager

## Dependencies
- Direct3D 8 API (IDirect3DDevice8, IDirect3DSurface8)
- W3D engine components (DX8Wrapper, W3DShaderManager)
- Game engine systems (View, Display, Camera)
- Memory management (GameMemory)
- Rendering infrastructure (SortingRendererClass)
