# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8webbrowser.cpp

## Purpose
Implements a Direct3D 8 embedded web browser wrapper for the game engine.

## Responsibilities
- Initializes and shuts down the embedded browser
- Creates and destroys browser instances
- Updates and renders browser content
- Navigates to URLs in existing browsers

## Key Types
- `DX8WebBrowser` (Class): Main browser wrapper class
- `IFEBrowserEngine2Ptr` (Type): COM smart pointer to browser engine

## Key Functions
### `Initialize`
- Purpose: Initializes COM and creates browser engine instance
- Calls: `CoInitialize`, `pBrowser.CreateInstance`, `pBrowser->Initialize`, `pBrowser->put_BadPageURL`, etc.

### `Shutdown`
- Purpose: Shuts down the browser and releases resources
- Calls: `pBrowser->Shutdown`, `CoUninitialize`

### `Update`
- Purpose: Updates browser image surfaces
- Calls: `pBrowser->D3DUpdate`

### `Render`
- Purpose: Draws all browsers to the back buffer
- Calls: `pBrowser->D3DRender`

### `CreateBrowser`
- Purpose: Creates a new browser window
- Calls: `pBrowser->CreateBrowser`, `pBrowser->SetUpdateRate`

### `DestroyBrowser`
- Purpose: Destroys a browser instance
- Calls: `pBrowser->DestroyBrowser`

### `Is_Browser_Open`
- Purpose: Checks if a browser is open
- Calls: `pBrowser->IsOpen`

### `Navigate`
- Purpose: Navigates to a URL in a browser
- Calls: `pBrowser->Navigate`

## Globals
- `pBrowser` (IFEBrowserEngine2Ptr): Global browser engine instance
- `hWnd` (HWND): Window handle for the browser

## Dependencies
- `dx8webbrowser.h`, `ww3d.h`, `dx8wrapper.h`
- COM interfaces (`IFEBrowserEngine2Ptr`)
- BrowserEngine.DLL (imported via `#import`)
