# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DWebBrowser.cpp

## Purpose
Handles creation and management of web browser windows within the W3D game engine.

## Responsibilities
- Creates and destroys web browser windows
- Manages browser window positioning and sizing
- Handles URL resolution for browser content
- Interfaces with DirectX 8 web browser components

## Key Types
- W3DWebBrowser (Class): Web browser wrapper for the game engine
- WebBrowserURL (Struct): URL data structure

## Key Functions
### W3DWebBrowser::createBrowserWindow
- Purpose: Creates a browser window with specified tag and position
- Calls: findURL, DX8WebBrowser::CreateBrowser

### W3DWebBrowser::closeBrowserWindow
- Purpose: Destroys a browser window associated with a game window
- Calls: DX8WebBrowser::DestroyBrowser

## Globals
None

## Dependencies
- W3DDevice/GameClient/W3DWebBrowser.h
- WW3D2/Texture.h
- WW3D2/TextureLoader.h
- WW3D2/SurfaceClass.h
- GameClient/Image.h
- GameClient/GameWindow.h
- vector2i.h
- d3dx8.h
- WW3D2/dx8wrapper.h
- WW3D2/dx8WebBrowser.h
