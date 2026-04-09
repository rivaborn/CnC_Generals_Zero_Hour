# Generals/Code/Tools/GUIEdit/Source/WinMain.cpp

## Purpose
Entry point and Windows message loop for the GUIEdit tool, a GUI layout editor for Command & Conquer Generals.

## Responsibilities
- Registers window class and creates main application window
- Handles Windows messages (commands, keyboard input, etc.)
- Manages application lifecycle (init/shutdown)
- Processes menu commands for file operations and editor functions
- Maintains editor state and updates

## Key Types
- None (procedural file)

## Key Functions
### WinMain
- Purpose: Application entry point that initializes resources and runs message loop
- Calls: registerClass, initInstance, DEBUG_INIT, initMemoryManager, TheEditor->init, TheEditor->update, shutdownMemoryManager, DEBUG_SHUTDOWN

### WndProc
- Purpose: Window procedure handling messages for the main window
- Calls: TheEditor->menuExit, TheEditor->menuNew, TheEditor->menuOpen, TheEditor->menuSave, TheEditor->menuSaveAs, TheEditor->menuCopy, TheEditor->menuCut, TheEditor->menuPaste, TheEditor->setShowHiddenOutlines, TheEditor->setShowSeeThruOutlines, TheEditor->setMode, TheEditWindow->getBackgroundColor, SelectColor, TheEditWindow->setBackgroundColor, TheDefaultScheme->openDialog, TheEditor->clearSelections, TheEditor->deleteSelected, TheEditor->gridSnapLocation, TheEditor->dragMoveSelectedWindows, TheEditor->getStatusBarWindowHandle, MoveWindow

### AboutCallback
- Purpose: Dialog procedure for the About box
- Calls: EndDialog

### initInstance
- Purpose: Creates and displays the main application window
- Calls: CreateWindowEx, ShowWindow, UpdateWindow

### registerClass
- Purpose: Registers the window class with Windows
- Calls: RegisterClassEx, LoadIcon, LoadCursor, GetStockObject

## Globals
- szWindowClass (char*): Window class name
- ApplicationHInstance (HINSTANCE): Main application instance handle
- ApplicationHWnd (HWND): Main application window handle
- TheWin32Mouse (Win32Mouse*): Win32 mouse interface
- gAppPrefix (char*): Debug log file prefix
- g_strFile (const Char*): Path to Generals.str file
- g_csfFile (const Char*): Path to Generals.csf file

## Dependencies
- Windows.h, commctrl.h
- Common/Debug.h, Common/GameMemory.h, Common/GameEngine.h
- GameClient/GameWindowManager.h
- Win32Device/GameClient/Win32Mouse.h
- Resource.h, Lib/BaseType.h
- GUIEdit.h, EditWindow.h, DialogProc.h, LayoutScheme.h
