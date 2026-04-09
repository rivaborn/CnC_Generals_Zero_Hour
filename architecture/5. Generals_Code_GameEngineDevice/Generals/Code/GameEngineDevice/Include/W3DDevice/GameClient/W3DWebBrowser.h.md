# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DWebBrowser.h

## Purpose
Header for W3DWebBrowser class, a WebBrowser subclass for rendering web content in the W3D game engine.

## Responsibilities
- Provides W3D-specific web browser functionality
- Manages browser window creation/closure within GameWindow
- Inherits core web browsing capabilities from WebBrowser

## Key Types
- W3DWebBrowser (Class): W3D-specific web browser implementation
- TextureClass (Class): Not inferable
- Image (Class): Not inferable
- GameWindow (Class): Not inferable

## Key Functions
### W3DWebBrowser()
- Purpose: Default constructor
- Calls: None

### createBrowserWindow(char *url, GameWindow *win)
- Purpose: Creates a browser window with specified URL in given GameWindow
- Calls: None (implementation in .cpp)

### closeBrowserWindow(GameWindow *win)
- Purpose: Closes browser window associated with given GameWindow
- Calls: None (implementation in .cpp)

## Globals
None

## Dependencies
- "GameNetwork/WOLBrowser/WebBrowser.h" (WebBrowser base class)
- TextureClass, Image, GameWindow (forward declarations)
