# GeneralsMD/Code/GameEngine/Include/GameNetwork/WOLBrowser/WebBrowser.h

## Purpose
Defines the WebBrowser subsystem interface for embedded browser functionality in the game.

## Responsibilities
- Manages embedded web browser instances via COM interface
- Handles URL tracking and parsing
- Provides browser window creation/closure
- Implements COM IUnknown and IBrowserDispatch interfaces

## Key Types
- **WebBrowserURL (Class)**: Represents a URL entry with tag and URL string
- **WebBrowserURLMagicEnum (Enum)**: Not inferable (empty)
- **WebBrowser (Class)**: Main browser subsystem interface
- **GameWindow (Class)**: External window reference (forward declared)

## Key Functions
### WebBrowser::init
- Purpose: Initializes the browser subsystem
- Calls: Not inferable

### WebBrowser::createBrowserWindow
- Purpose: Creates an embedded browser window for a GameWindow
- Calls: Not inferable

### WebBrowser::makeNewURL
- Purpose: Creates a new WebBrowserURL instance
- Calls: Not inferable

### WebBrowser::QueryInterface
- Purpose: COM QueryInterface implementation
- Calls: Not inferable

## Globals
- **TheWebBrowser (CComObject<WebBrowser>*)**: Singleton instance of the browser subsystem

## Dependencies
- Common/SubsystemInterface.h
- atlbase.h, windows.h
- Common/GameMemory.h
- EABrowserDispatch/BrowserDispatch.h
- FEBDispatch.h
