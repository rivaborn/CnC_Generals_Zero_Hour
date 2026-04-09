# GeneralsMD/Code/GameEngine/Source/GameNetwork/WOLBrowser/WebBrowser.cpp

## Purpose
Manages an embedded WebBrowser component for in-game web content, handling COM/OLE initialization and URL management.

## Responsibilities
- Initializes and shuts down COM/OLE via global `OLEInitializer`
- Manages WebBrowser instance lifecycle (creation/destruction)
- Loads and parses URLs from `Webpages.ini`
- Implements COM interfaces (`IUnknown`, `IBrowserDispatch`) for browser control

## Key Types
- **OLEInitializer (Class)**: Wraps COM/OLE initialization/shutdown
- **WebBrowserURL (Struct)**: Represents a URL entry with tag/URL fields
- **WebBrowser (Class)**: Main browser component implementing COM interfaces

## Key Functions
### WebBrowser::init
- Purpose: Loads URL list from `Webpages.ini`
- Calls: `INI::load`

### WebBrowser::QueryInterface
- Purpose: COM interface query implementation
- Calls: None

### WebBrowser::Release
- Purpose: COM reference counting and cleanup
- Calls: None

### WebBrowser::TestMethod
- Purpose: Test method for debugging
- Calls: None

## Globals
- **g_OLEInitializer (OLEInitializer)**: Global COM/OLE initializer
- **_Module (CComModule)**: COM module instance
- **TheWebBrowser (CComObject<WebBrowser>*)**: Singleton browser instance

## Dependencies
- `WebBrowser.h`, `GameWindow.h`, `Display.h`
- COM interfaces (`IUnknown`, `IBrowserDispatch`)
- INI parsing system (`INI`, `FieldParse`)
