# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetPushButton.cpp

## Purpose
Handles input and system message processing for push button GUI gadgets in the game.

## Responsibilities
- Processes mouse and keyboard input for buttons
- Manages button states (selected, hilited, check-like)
- Handles audio feedback for button clicks
- Provides utility functions for button configuration

## Key Types
- `PushButtonData` (struct): Stores button-specific data (border, clock, overlay, sound, user data)
- `buttonTriggersOnMouseDown` (function): Determines if button triggers on mouse down

## Key Functions
### `GadgetPushButtonInput`
- Purpose: Handles input messages for push buttons
- Calls: `buttonTriggersOnMouseDown`, `TheWindowManager->winSendSystemMsg`, `TheAudio->addAudioEvent`

### `GadgetPushButtonSystem`
- Purpose: Handles system messages for push buttons
- Calls: `TheWindowManager->winSendSystemMsg`

### `GadgetCheckLikeButtonSetVisualCheck`
- Purpose: Sets visual checked state for check-like buttons
- Calls: None

### `GadgetButtonSetText`
- Purpose: Sets button text label
- Calls: `TheWindowManager->winSendSystemMsg`

### `GadgetButtonSetBorder`
- Purpose: Configures button border drawing
- Calls: `getNewPushButtonData`

### `GadgetButtonDrawClock`
- Purpose: Configures clock drawing on button
- Calls: `getNewPushButtonData`

### `GadgetButtonSetData`
- Purpose: Sets user data on button
- Calls: `getNewPushButtonData`

## Globals
- None

## Dependencies
- `GameWindow`, `WinInstanceData`, `AudioEventRTS`, `TheWindowManager`, `TheAudio`
- Key includes: `PreRTS.h`, `Common/AudioEventRTS.h`, `GameClient/Gadget.h`
