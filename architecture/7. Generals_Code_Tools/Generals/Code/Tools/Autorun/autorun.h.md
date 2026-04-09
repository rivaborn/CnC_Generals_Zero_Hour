# Generals/Code/Tools/Autorun/autorun.h

## Purpose
Header file defining classes and types for the autorun tool in Command & Conquer Generals.

## Responsibilities
- Defines language types and constants
- Declares LaunchObjectClass for program execution
- Declares Window and MainWindow classes for GUI handling
- Declares Main class for application control
- Provides registry and path constants

## Key Types
- LanguageType (Enum): language identifiers (USA, UK, GER, etc.)
- LaunchObjectClass (Class): handles program launching with path/args
- Window (Class): base abstract window class
- MainWindow (Class): concrete window implementation
- Main (Class): application control class

## Key Functions
### LaunchObjectClass::Launch
- Purpose: Execute the configured program
- Calls: Not inferable

### MainWindow::Window_Proc
- Purpose: Handle window messages
- Calls: Not inferable

### MainWindow::Run_Game
- Purpose: Launch the main game executable
- Calls: Not inferable

## Globals
- Language (int): current language setting
- LaunchObject (LaunchObjectClass): global launch object instance

## Dependencies
- `<tchar.h>`, `<string.h>`, `<stdio.h>`, `<stdlib.h>`
- `ttfont.h`
- Windows API types (HWND, HINSTANCE, etc.)
- Registry path constants
