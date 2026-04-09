# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DWebBrowser.h

## Purpose
Header file declaring the W3DWebBrowser class, a WebBrowser subclass for rendering web content in the game engine.

## Responsibilities
- Defines W3DWebBrowser class interface
- Declares browser window creation/closure methods
- Integrates with GameWindow for rendering

## Key Types
- W3DWebBrowser (Class): Web browser component for in-game web content display
- TextureClass (Class): Not inferable (forward declaration)
- Image (Class): Not inferable (forward declaration)
- GameWindow (Class): Not inferable (forward declaration)

## Key Functions
### W3DWebBrowser()
- Purpose: Default constructor for W3DWebBrowser
- Calls: Not inferable

### createBrowserWindow(char *url, GameWindow *win)
- Purpose: Creates a browser window with specified URL in given GameWindow
- Calls: Not inferable

### closeBrowserWindow(GameWindow *win)
- Purpose: Closes browser window associated with given GameWindow
- Calls: Not inferable

## Globals
None

## Dependencies
- "GameNetwork/WOLBrowser/WebBrowser.h" (WebBrowser base class)
- TextureClass, Image, GameWindow (forward declarations)
