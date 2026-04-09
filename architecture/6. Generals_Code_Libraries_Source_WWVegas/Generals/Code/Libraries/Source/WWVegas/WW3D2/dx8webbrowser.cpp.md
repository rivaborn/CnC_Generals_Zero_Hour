# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8webbrowser.cpp

## Purpose
Implements a Direct3D 8 embedded web browser wrapper for the game engine.

## Responsibilities
- Initializes and shuts down the embedded browser
- Manages browser window creation/destruction
- Updates and renders browser content into the game's back buffer
- Handles navigation and browser state queries

## Key Types
- `DX8WebBrowser` (Class): Main browser wrapper class
- `IFEBrowserEngine2Ptr` (Type): COM smart pointer to the browser engine

## Key Functions
### `Initialize`
- Purpose: Initializes COM and creates the browser engine instance
- Calls: `CoInitialize`, `pBrowser.CreateInstance`, `pBrowser->Initialize`, `pBrowser->put_BadPageURL`, etc.

### `Shutdown`
- Purpose: Cleans up browser resources and uninitializes COM
- Calls: `pBrowser->Shutdown`, `CoUninitialize`

### `Update`
- Purpose: Updates browser image surfaces
- Calls: `pBrowser->D3DUpdate`

### `Render`
- Purpose: Renders all browsers to the back buffer
- Calls: `pBrowser->D3DRender`

### `CreateBrowser`
- Purpose: Creates a new browser window instance
- Calls: `pBrowser->CreateBrowser`, `pBrowser->SetUpdateRate`

### `DestroyBrowser`
- Purpose: Destroys a browser instance
- Calls: `pBrowser->DestroyBrowser`

### `Is_Browser_Open`
- Purpose: Checks if a browser is open
- Calls: `pBrowser->IsOpen`

### `Navigate`
- Purpose: Navigates a browser to a URL
- Calls: `pBrowser->Navigate`

## Globals
- `pBrowser` (IFEBrowserEngine2Ptr): Global browser engine instance pointer
- `hWnd` (HWND): Static window handle for the browser

## Dependencies
- `dx8webbrowser.h`, `ww3d.h`, `dx8wrapper.h`
- COM interfaces (`IFEBrowserEngine2Ptr`)
- BrowserEngine.DLL (imported via #import)
- `_bstr_t` (ATL string type)
