# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DMouse.cpp

## Purpose
Handles mouse cursor rendering and input in the W3D (Westwood 3D) game engine, supporting multiple cursor types and rendering modes.

## Responsibilities
- Manages different cursor rendering modes (Windows, DirectX8, W3D, Polygon)
- Loads and unloads cursor assets (textures, models, animations)
- Handles cursor animation and positioning
- Provides thread-safe cursor updates via a dedicated mouse thread
- Integrates with the game's display and UI systems

## Key Types
- **MouseThreadClass (Class)**: Thread class for polling mouse input and updating cursor position
- **W3DMouse (Class)**: Main mouse handling class (inherits from base Mouse class)
- **RedrawMode (Enum)**: Not inferable (likely defines rendering modes)

## Key Functions
### `MouseThreadClass::Thread_Function`
- Purpose: Polls mouse and updates cursor position in a separate thread
- Calls: `TheMouse->draw()`

### `W3DMouse::init`
- Purpose: Initializes mouse system and starts update thread if needed
- Calls: `Win32Mouse::init()`, `thread.Execute()`

### `W3DMouse::draw`
- Purpose: Renders cursor based on current mode and position
- Calls: `setCursor()`, `TheDisplay->drawImage()`, `WW3D::Render()`

### `W3DMouse::setCursor`
- Purpose: Changes current cursor type and updates rendering
- Calls: `Win32Mouse::setCursor()`, `releaseD3DCursorTextures()`, `loadD3DCursorTextures()`

### `W3DMouse::setRedrawMode`
- Purpose: Switches between different cursor rendering modes
- Calls: `freeD3DAssets()`, `freeW3DAssets()`, `freePolygonAssets()`, `initW3DAssets()`, `initPolygonAssets()`

## Globals
- **mutex (CriticalSectionClass)**: Thread synchronization for cursor updates
- **isThread (Bool)**: Flag indicating if mouse thread is active
- **cursorTextures (TextureClass**)**: Array of cursor textures for different types
- **cursorImages (Image**)**: Array of cursor images for polygon rendering
- **cursorModels (RenderObjClass**)**: Array of 3D cursor models
- **cursorAnims (HAnimClass**)**: Array of cursor animations
- **thread (MouseThreadClass)**: Mouse update thread instance
- **ApplicationHWnd (HWND)**: Handle to application window

## Dependencies
- Key includes: `Common/GameMemory.h`, `WW3D2/DX8Wrapper.h`, `WW3D2/RendObj.h`, `WW3D2/HAnim.h`, `WW3D2/Camera.h`, `assetmgr.h`, `W3DDevice/Common/W3DConvert.h`, `W3DDevice/GameClient/W3DMouse.h`, `W3DDevice/GameClient/W3DDisplay.h`, `W3DDevice/GameClient/W3DAssetManager.h`, `W3DDevice/GameClient/W3DScene.h`, `GameClient/Display.h`, `GameClient/Image.h`, `GameClient/InGameUI.h`, `mutex.h`, `thread.h`
- External symbols: `TheMouse`, `TheMappedImageCollection`, `TheDisplay`, `TheInGameUI`, `W3DDisplay::m_assetManager`, `W3DDisplay::m_3DInterfaceScene`, `DX8Wrapper::_Get_D3D_Device8()`
