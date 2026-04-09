# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/IMEManager.cpp

## Purpose
Manages Input Method Editor (IME) functionality for text input in the game, particularly for non-Latin character sets.

## Responsibilities
- Handles IME message processing and context management
- Manages composition string and candidate list display
- Controls IME window attachment/detachment and enabling/disabling
- Provides interface for retrieving IME state and candidate information

## Key Types
- **IMEManager (Class)**: Main IME management class implementing IMEManagerInterface
- **(anonymous enum)**: Contains MAX_COMPSTRINGLEN constant
- **MessageInfo (struct)**: Stores message name-value pairs for debugging
- **MAX_COMPSTRINGLEN (Enum)**: Maximum composition string length constant

## Key Functions
### IMEManager::serviceIMEMessage
- Purpose: Processes Windows IME messages
- Calls: Various Windows IME API functions, updateCompositionString, updateCandidateList

### IMEManager::updateCandidateList
- Purpose: Updates the candidate list from IME context
- Calls: ImmGetCandidateListCountW/A, ImmGetCandidateListW/A, updateListBox

### IMEManager::convertToUnicode
- Purpose: Converts multibyte characters to Unicode strings
- Calls: MultiByteToWideChar

## Globals
- **ApplicationHWnd (HWND)**: The game's application window handle
- **IMECandidateWindowLineSpacing (Int)**: Spacing between candidate list items
- **TheIMEManager (IMEManagerInterface*)**: Global IME manager instance

## Dependencies
- Windows.h, mbstring.h
- Common/Debug.h, Common/Language.h, Common/UnicodeString.h
- GameClient/Display.h, GameClient/GameWindow.h, GameClient/GameWindowManager.h
- GameClient/GadgetListBox.h, GameClient/IMEManager.h, GameClient/Mouse.h
- GameClient/Color.h, Common/NameKeyGenerator.h
