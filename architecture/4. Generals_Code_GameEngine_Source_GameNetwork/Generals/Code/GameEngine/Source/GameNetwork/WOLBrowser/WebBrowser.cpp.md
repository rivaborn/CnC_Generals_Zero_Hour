# Generals/Code/GameEngine/Source/GameNetwork/WOLBrowser/WebBrowser.cpp

## Purpose
Manages an embedded web browser component for the game, handling COM/OLE initialization and URL management.

## Responsibilities
- Initializes and shuts down COM/OLE for the web browser
- Manages a list of web page URLs loaded from an INI file
- Implements COM interfaces (IUnknown, IBrowserDispatch) for the browser object
- Provides reference counting for COM object lifetime management
- Maintains a global singleton instance of the web browser

## Key Types
- **OLEInitializer (Class)**: Wrapper for COM/OLE initialization and cleanup
- **WebBrowserURL (Class)**: Represents a single URL entry with tag and URL string
- **WebBrowser (Class)**: Main COM object implementing the browser interface
- **IBrowserDispatch (Interface)**: COM interface for browser control (external)

## Key Functions
### WebBrowser::init
- Purpose: Loads URL configuration from Webpages.ini
- Calls: INI::load

### WebBrowser::QueryInterface
- Purpose: Implements COM QueryInterface for IUnknown and IBrowserDispatch
- Calls: None

### WebBrowser::AddRef
- Purpose: Increments reference count for COM object
- Calls: None

### WebBrowser::Release
- Purpose: Decrements reference count and deletes object when reaching zero
- Calls: None

## Globals
- **g_OLEInitializer (OLEInitializer)**: Global COM/OLE initializer instance
- **_Module (CComModule)**: ATL module object for COM support
- **TheWebBrowser (CComObject<WebBrowser>*)**: Global pointer to the web browser instance

## Dependencies
- **PreRTS.h**: Game engine precompiled header
- **WebBrowser.h**: Header for this component
- **GameWindow.h**: Game window management
- **Display.h**: Display system
- **ATL/COM headers**: For COM/OLE support (CComModule, IUnknown, etc.)
- **INI class**: For configuration file parsing
