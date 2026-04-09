# Generals/Code/Tools/WorldBuilder/include/SplashScreen.h

## Purpose
Defines a splash screen dialog class for displaying loading progress text in WorldBuilder.

## Responsibilities
- Manages splash screen UI rendering
- Handles text output positioning and display
- Provides loading progress feedback via string resources

## Key Types
- SplashScreen (Class): Splash screen dialog with text output capabilities

## Key Functions
### SplashScreen()
- Purpose: Constructor for SplashScreen class
- Calls: Not inferable

### setTextOutputLocation()
- Purpose: Sets the rectangle where loading text will be displayed
- Calls: Not inferable

### outputText()
- Purpose: Displays a string resource as loading progress text
- Calls: Not inferable

### OnPaint()
- Purpose: Handles splash screen painting/rendering
- Calls: Not inferable

## Globals
- None

## Dependencies
- CDialog (MFC class)
- CRect (MFC class)
- CString (MFC class)
- CFont (MFC class)
- afx_msg (MFC macro)
- DECLARE_MESSAGE_MAP() (MFC macro)
