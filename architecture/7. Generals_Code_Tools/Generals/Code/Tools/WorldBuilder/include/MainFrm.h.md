# Generals/Code/Tools/WorldBuilder/include/MainFrm.h

## Purpose
Defines the main frame window class for the WorldBuilder tool, managing UI components and tool options.

## Responsibilities
- Manages the main application window and its child controls (toolbar, status bar).
- Hosts various tool option panels (brush, terrain, objects, etc.).
- Handles window positioning, autosave functionality, and camera changes.
- Provides access to global tool state via static methods.

## Key Types
- **CMainFrame (Class)**: Main application frame window.
- **LayersList (Class)**: Not inferable (forward declaration only).

## Key Functions
### CMainFrame::PreCreateWindow
- Purpose: Customizes window creation parameters.
- Calls: Not inferable.

### CMainFrame::showOptionsDialog
- Purpose: Displays a tool-specific options dialog.
- Calls: Not inferable.

### CMainFrame::handleCameraChange
- Purpose: Handles camera view changes.
- Calls: Not inferable.

### CMainFrame::OnTimer
- Purpose: Handles timer events (e.g., autosave).
- Calls: Not inferable.

## Globals
- **TheMainFrame (CMainFrame*)**: Singleton instance of the main frame.

## Dependencies
- MFC framework (CFrameWnd, CToolBar, etc.).
- Custom tool option classes (BrushOptions, TerrainMaterial, etc.).
- BaseType.h for core types.
