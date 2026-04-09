# Generals/Code/Tools/WorldBuilder/src/WorldBuilder.cpp

## Purpose
Main application file for WorldBuilder, the map editor tool for Command & Conquer Generals.

## Responsibilities
- Initializes the application and subsystems
- Manages tool selection and activation
- Handles document templates and file operations
- Implements the main message loop and UI commands

## Key Types
- **WBGameFileClass (Class)**: Extends GameFileClass to handle WB-specific file operations
- **WB_W3DFileSystem (Class)**: Extends W3DFileSystem for WB file access
- **CAboutDlg (Class)**: Dialog for the "About" box
- **(anonymous enum) (Enum)**: Dialog resource IDs
- **IDD (Enum)**: Dialog resource IDs

## Key Functions
### initSubsystem
- Purpose: Initializes a subsystem and adds it to the subsystem list
- Calls: TheSubsystemListRecord.initSubsystem

### WBGameFileClass::Set_Name
- Purpose: Sets the file name and checks for GDI asset availability
- Calls: GameFileClass::Set_Name, TheFileSystem->doesFileExist

### WB_W3DFileSystem::Get_File
- Purpose: Retrieves a file with the specified filename
- Calls: WBGameFileClass constructor

### CWorldBuilderApp::InitInstance
- Purpose: Initializes the application instance
- Calls: EulaDialog::DoModal, DEBUG_INIT, initMemoryManager, SplashScreen methods, initSubsystem, INI methods, etc.

### CWorldBuilderApp::OnCmdMsg
- Purpose: Handles command messages for tools
- Calls: Tool methods (activate, deactivate), CWinApp::OnCmdMsg

### CWorldBuilderApp::selectPointerTool
- Purpose: Sets the active tool to the pointer and clears selection
- Calls: setActiveTool, m_pointerTool.clearSelection

### CWorldBuilderApp::setActiveTool
- Purpose: Activates a new tool and deactivates the current one
- Calls: Tool::activate, Tool::deactivate

### CWorldBuilderApp::updateCurTool
- Purpose: Updates the current tool based on key modifiers
- Calls: Tool::activate, ::GetAsyncKeyState

### CWorldBuilderApp::ExitInstance
- Purpose: Cleans up resources when the application exits
- Calls: WriteProfileString, ScriptList::reset, TheSubsystemListRecord.shutdownAll, etc.

## Globals
- **TheSubsystemListRecord (SubsystemInterfaceList)**: Records all initialized subsystems
- **TheWin32Mouse (Win32Mouse*)**: Pointer to the Win32 mouse handler
- **gAppPrefix (char*)**: Prefix for WB debug log files
- **g_strFile (const Char*)**: Path to the string file
- **g_csfFile (const Char*)**: Path to the CSF file template
- **theApp (CWorldBuilderApp)**: The single instance of the application
- **ApplicationHWnd (HWND)**: Handle to the application window
- **ApplicationHInstance (HINSTANCE)**: Instance handle for the application
- **gFirstCP (Int)**: First memory checkpoint for leak detection

## Dependencies
- Key includes: stdafx.h, WorldBuilder.h, EulaDialog.h, MainFrm.h, OpenMap.h, SplashScreen.h, Textureloader.h, WorldBuilderDoc.h, WorldBuilderView.h, WBFrameWnd.h, WbView3d.h, W3DDevice/GameClient/W3DFileSystem.h, common/GlobalData.h, WHeightMapEdit.h, Common/FileSystem.h, Common/ArchiveFileSystem.h, Common/LocalFileSystem.h, Common/CDManager.h, Common
