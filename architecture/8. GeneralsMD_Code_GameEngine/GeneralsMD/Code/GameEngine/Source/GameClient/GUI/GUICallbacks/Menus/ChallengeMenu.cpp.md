# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ChallengeMenu.cpp

## Purpose
Manages the Challenge Mode menu UI, allowing players to select generals and start campaigns.

## Responsibilities
- Initializes, updates, and shuts down the Challenge Mode menu
- Handles general selection and campaign setup
- Manages bio text display with teletype animation
- Processes user input (mouse/keyboard) for menu navigation

## Key Types
- **SkirmishGameInfo** (Global): Stores game info for skirmish/challenge mode
- **GeneralPersona** (External): Represents a playable general with stats and bio data
- **GameWindow** (External): Base class for UI elements
- **WindowVideoManager** (Static): Manages video playback in the menu

## Key Functions
### ChallengeMenuInit
- Purpose: Initializes menu UI elements and game state
- Calls: `setEnabledButtons`, `TheWindowManager->winGetWindowFromId`, `TheCampaignManager->setCampaign`

### ChallengeMenuUpdate
- Purpose: Handles periodic menu updates (bio text animation, transitions)
- Calls: `updateBio`, `TheTransitionHandler->isFinished`, `wndVideoManager->update`

### ChallengeMenuSystem
- Purpose: Processes system messages (mouse events, selections)
- Calls: `findPositionButton`, `setGeneralBio`, `GadgetCheckBoxToggle`, `TheAudio->addAudioEvent`

### updateBio
- Purpose: Animates bio text display character-by-character
- Calls: `GadgetStaticTextGetText`, `GadgetStaticTextSetText`

## Globals
- **TheChallengeGameInfo** (SkirmishGameInfo*): Stores challenge game configuration
- **buttonGeneralPosition** (GameWindow[]): Array of general selection buttons
- **lastButtonIndex** (Int): Tracks currently selected general
- **bioTextPosition** (Int): Tracks bio text animation progress
- **wndVideoManager** (WindowVideoManager*): Manages menu video playback

## Dependencies
- Key includes: `GameClient/Gadget.h`, `GameClient/CampaignManager.h`, `GameClient/ChallengeGenerals.h`
- External symbols: `TheWindowManager`, `TheAudio`, `TheCampaignManager`, `TheChallengeGenerals`
