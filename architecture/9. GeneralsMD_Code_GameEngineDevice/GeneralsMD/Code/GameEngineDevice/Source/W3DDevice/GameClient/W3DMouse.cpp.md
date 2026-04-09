# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DMouse.cpp

## Purpose
Handles mouse cursor rendering and input in the W3D (Westwood 3D) game engine, supporting multiple cursor types and rendering modes.

## Responsibilities
- Manages mouse cursor rendering in different modes (Windows, DX8, W3D, Polygon)
- Handles cursor asset loading/unloading (textures, models, animations)
- Implements a background thread for cursor updates in DX8 mode
- Provides cursor direction handling for directional cursors
- Renders cursor tooltips and text

## Key Types
- **MouseThreadClass (Class)**: Background thread for DX8 cursor updates
- **W3DMouse (Class)**: Main mouse handling class (inherits from Mouse)
- **None**: No other significant types defined

## Key Functions
### MouseThreadClass::Thread_Function
- Purpose: Background thread that polls mouse and updates cursor position
- Calls: TheMouse->draw()

### W3DMouse::draw
- Purpose: Renders the mouse cursor based on current mode
- Calls: setCursor(), TheDisplay->drawImage(), WW3D::Render(), drawCursorText(), drawTooltip()

### W3DMouse::setCursor
- Purpose: Changes the current mouse cursor type
- Calls: Win32Mouse::setCursor(), releaseD3DCursorTextures(), loadD3DCursorTextures(), SetCursor(), m_pDev->SetCursorProperties()

### W3DMouse::setRedrawMode
- Purpose: Switches between different cursor rendering modes
- Calls: setCursor(), freeD3DAssets(), freeW3DAssets(), freePolygonAssets(), initW3DAssets(), initPolygonAssets(), thread.Execute(), thread.Stop()

## Globals
- **mutex (CriticalSectionClass)**: Thread synchronization for cursor operations
- **isThread (Bool)**: Flag indicating if thread is active
- **cursorTextures (TextureClass**)**: Array of cursor textures for different types
- **cursorImages (const Image**)**: Array of cursor images for polygon rendering
- **cursorModels (RenderObjClass**)**: Array of cursor 3D models
- **cursorAnims (HAnimClass**)**: Array of cursor animations
- **thread (MouseThreadClass)**: Background thread instance
- **ApplicationHWnd (HWND)**: Global window handle

## Dependencies
- Common/GameMemory.h, WW3D2/DX8Wrapper.h, WW3D2/RendObj.h, WW3D2/HAnim.h, WW3D2/Camera.h
- assetmgr.h, W3DDevice/Common/W3DConvert.h, W3DDevice/GameClient/W3DMouse.h, W3DDevice/GameClient/W3DDisplay.h
- W3DDevice/GameClient/W3DAssetManager.h, W3DDevice/GameClient/W3DScene.h, GameClient/Display.h
- GameClient/Image.h, GameClient/InGameUI.h, mutex.h, thread.h
- DX8Wrapper, RenderObjClass, HAnimClass, CameraClass, AssetManagerClass, DisplayClass, ImageClass, InGameUIClass
