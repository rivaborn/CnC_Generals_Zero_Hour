# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/IMECandidate.cpp

## Purpose
Handles rendering and input for the IME (Input Method Editor) candidate window in the game UI.

## Responsibilities
- Manages candidate window drawing (text and background)
- Handles window system messages (creation/destruction)
- Displays candidate text with numbering and selection highlighting
- Manages DisplayString resource lifecycle

## Key Types
- None

## Key Functions
### IMECandidateWindowInput
- Purpose: Handles input messages for the candidate window
- Calls: None

### IMECandidateWindowSystem
- Purpose: Processes system messages for window creation/destruction
- Calls: TheDisplayStringManager->newDisplayString(), TheDisplayStringManager->freeDisplayString()

### IMECandidateTextAreaDraw
- Purpose: Renders candidate text items with numbering and selection highlighting
- Calls: window->winGetScreenPosition(), window->winGetSize(), window->winGetStatus(), window->winGetFont(), window->winGetEnabledTextColor(), window->winGetEnabledTextBorderColor(), window->winGetDisabledTextColor(), window->winGetDisabledTextBorderColor(), window->winGetHiliteTextColor(), window->winGetHiliteTextBorderColor(), TheWindowManager->winOpenRect(), Dstring->setFont(), Dstring->setClipRegion(), Dstring->setText(), Dstring->getWidth(), Dstring->draw(), ime->getCandidatePageStart(), ime->getCandidateCount(), ime->getCandidatePageSize(), ime->getSelectedCandidateIndex(), ime->getCandidate(), ime->getIndexBase()

### IMECandidateMainDraw
- Purpose: Draws the background and border of the candidate window
- Calls: window->winGetScreenPosition(), window->winGetSize(), window->winGetStatus(), window->winGetEnabledColor(), window->winGetEnabledBorderColor(), window->winGetDisabledColor(), window->winGetDisabledBorderColor(), window->winGetHiliteColor(), window->winGetHiliteBorderColor(), TheWindowManager->winOpenRect(), TheWindowManager->winFillRect()

## Globals
- IMECandidateWindowLineSpacing (Int): Spacing between candidate lines
- Dstring (DisplayString*): Shared display string resource for rendering

## Dependencies
- GameClient/GameWindow.h
- GameClient/Gadget.h
- GameClient/IMEManager.h
- GameClient/GameWindowManager.h
- GameClient/DisplayString.h
- GameClient/DisplayStringManager.h
- TheWindowManager, TheDisplayStringManager (external symbols)
