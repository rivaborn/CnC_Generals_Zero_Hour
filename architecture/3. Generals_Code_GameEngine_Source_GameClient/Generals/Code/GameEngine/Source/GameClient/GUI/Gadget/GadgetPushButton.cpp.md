# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetPushButton.cpp

## Purpose
Handles input, rendering, and state management for push button GUI gadgets in the game.

## Responsibilities
- Processes mouse/keyboard input for buttons (clicks, hover, keyboard navigation)
- Manages button states (selected, hilited, check-like toggles)
- Handles audio feedback for button interactions
- Provides utility functions for button configuration (text, borders, clocks, overlays)
- Manages button-specific user data storage

## Key Types
- **PushButtonData (struct)**: Stores button-specific data (borders, clocks, overlays, user data, alt sounds)
- **ClockType (enum)**: Defines clock drawing modes (NO_CLOCK, NORMAL_CLOCK, INVERSE_CLOCK)

## Key Functions
### GadgetPushButtonInput
- Purpose: Handles all input messages for push buttons
- Calls: TheWindowManager->winSendSystemMsg, TheAudio->addAudioEvent, TheWindowManager->winNextTab, TheWindowManager->winPrevTab

### GadgetPushButtonSystem
- Purpose: Processes system messages for push buttons
- Calls: window->winSetText, TheWindowManager->winSendSystemMsg

### GadgetCheckLikeButtonSetVisualCheck
- Purpose: Visually toggles check-like button state without sending messages
- Calls: None

### GadgetButtonSetText
- Purpose: Sets the text label for a button
- Calls: TheWindowManager->winSendSystemMsg

### getNewPushButtonData
- Purpose: Creates and initializes new PushButtonData
- Calls: NEW operator

## Globals
- **TheWindowManager (GameWindowManager**)**: Global window manager instance
- **TheAudio (GameAudio**)**: Global audio system instance

## Dependencies
- Common/AudioEventRTS.h, Common/Language.h, Common/GameAudio.h
- GameClient/Gadget.h, GameClient/GameWindowManager.h, GameClient/InGameUI.h
- PreRTS.h (engine precompiled header)
- External symbols: TheWindowManager, TheAudio, DEBUG_CRASH, NEW operator
