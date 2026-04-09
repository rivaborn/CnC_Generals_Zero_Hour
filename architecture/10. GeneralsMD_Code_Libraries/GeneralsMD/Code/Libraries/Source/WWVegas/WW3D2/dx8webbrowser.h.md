# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8webbrowser.h

## Purpose
Header file defining the DX8WebBrowser class, a wrapper for embedding a web browser in Direct3D 8.

## Responsibilities
- Declares the DX8WebBrowser class interface
- Defines constants for browser options
- Provides static methods for browser lifecycle management
- Exposes rendering and navigation functionality

## Key Types
- IDirect3DDevice8 (Class): Direct3D 8 device interface
- DX8WebBrowser (Class): Wrapper for embedded browser functionality

## Key Functions
### Initialize
- Purpose: Initializes the embedded browser system
- Calls: Not inferable

### Shutdown
- Purpose: Shuts down the embedded browser system
- Calls: Not inferable

### Update
- Purpose: Copies browser contexts to D3D image surfaces
- Calls: Not inferable

### Render
- Purpose: Draws all browsers to the backbuffer
- Calls: Not inferable

### CreateBrowser
- Purpose: Creates a new browser instance
- Calls: Not inferable

### DestroyBrowser
- Purpose: Destroys a browser instance
- Calls: Not inferable

### Is_Browser_Open
- Purpose: Checks if a browser with the specified name is open
- Calls: Not inferable

### Navigate
- Purpose: Navigates a browser to a specified URL
- Calls: Not inferable

## Globals
- hWnd (HWND): Stores the application window handle

## Dependencies
- windows.h
- d3d8.h
- BROWSEROPTION constants (defined in febrowserengine.h)
