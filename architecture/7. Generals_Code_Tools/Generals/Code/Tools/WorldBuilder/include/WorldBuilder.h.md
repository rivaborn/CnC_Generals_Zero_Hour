# Generals/Code/Tools/WorldBuilder/include/WorldBuilder.h

## Purpose
Main header for the WorldBuilder application, defining the core CWorldBuilderApp class and tool management.

## Responsibilities
- Manages tool selection and activation
- Handles map object clipboard operations
- Provides application-wide state (current directory, active tool)
- Coordinates with MFC document template system

## Key Types
- CWorldBuilderApp (Class): Main application class managing tools and state
- Tool (Class): Base class for editing tools (not defined here)
- MapObject (Class): Represents map objects (not defined here)
- (anonymous enum): Constants for 3D view dimensions and max objects

## Key Functions
### WbApp
- Purpose: Global accessor for the WorldBuilder application instance
- Calls: AfxGetApp()

### CWorldBuilderApp::setActiveTool
- Purpose: Activates a tool and updates UI state
- Calls: Not inferable

### CWorldBuilderApp::updateCurTool
- Purpose: Handles keyboard overrides for tool selection
- Calls: Not inferable

### CWorldBuilderApp::OnCmdMsg
- Purpose: Routes command messages to appropriate handlers
- Calls: Not inferable

## Globals
- m_3dtemplate (CDocTemplate*): Document template for 3D views
- m_pasteMapObjList (MapObject*): Clipboard for copied/cut map objects
- m_currentDirectory (AsciiString): Current working directory
- m_lockCurTool (Int): Flag to lock current tool

## Dependencies
- MFC framework (CWinApp, CDocTemplate, CCmdUI)
- Tool subclasses (BrushTool, TileTool, etc.)
- Common utilities (STLTypedefs, Debug)
- Resource.h for UI elements
