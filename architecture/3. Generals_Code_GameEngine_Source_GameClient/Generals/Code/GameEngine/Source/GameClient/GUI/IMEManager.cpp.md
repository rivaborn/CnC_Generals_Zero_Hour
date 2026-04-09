# Generals/Code/GameEngine/Source/GameClient/GUI/IMEManager.cpp

## Purpose
Manages Input Method Editor (IME) functionality for text input in the game, particularly for non-Latin character sets.

## Responsibilities
- Handles IME message processing and context management
- Manages composition string and candidate list display
- Controls IME attachment to game windows
- Provides interface for IME state queries
- Manages candidate and status windows

## Key Types
- **IMEManager (Class)**: Main IME management class implementing IMEManagerInterface
- **(anonymous enum)**: Contains MAX_COMPSTRINGLEN constant
- **MessageInfo (struct)**: Stores message name-value pairs for debugging
- **MAX_COMPSTRINGLEN (Enum)**: Maximum composition string length constant

## Key Functions
### IMEManager::serviceIMEMessage
- Purpose: Processes Windows IME messages
- Calls: Various Windows IME API functions, internal update methods

### IMEManager::updateCandidateList
- Purpose: Updates the candidate list from IME context
- Calls: ImmGetCandidateListA/W, convertToUnicode

### IMEManager::updateCompositionString
- Purpose: Updates composition string from IME context
- Calls: ImmGetCompositionStringW

### IMEManager::openCandidateList
- Purpose: Opens the candidate selection window
- Calls: updateCandidateList, resizeCandidateWindow, window manager methods

## Globals
- **ApplicationHWnd (HWND)**: Application window handle
- **IMECandidateWindowLineSpacing (Int)**: Spacing between candidate items
- **TheIMEManager (IMEManagerInterface*)**: Global IME manager instance

## Dependencies
- Windows.h, imm.h (IME APIs)
- GameClient headers (Display, GameWindow, etc.)
- Common headers (Debug, Language, UnicodeString)
- NameKeyGenerator for window naming
