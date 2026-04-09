# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ScoreScreen.cpp

## Purpose
Handles the score screen UI for single-player, skirmish, LAN, internet, and replay games in Command & Conquer Generals.

## Responsibilities
- Initialize and shutdown the score screen UI
- Populate score screen with player statistics (units built/destroyed, resources, etc.)
- Manage game transitions (e.g., campaign progression)
- Handle user input for score screen controls
- Display battle honors and challenge medals

## Key Types
- **ScoreGather (Struct)**: Tracks player statistics (money earned/spent, units/buildings built/destroyed/lost, side image)
- **SCORESCREEN_SINGLEPLAYER/SCORESCREEN_SKIRMISH/SCORESCREEN_LAN/SCORESCREEN_INTERNET/SCORESCREEN_REPLAY (Enums)**: Score screen types
- **USA_FRIEND/CHINA_FRIEND/GLA_FRIEND/USA_ENEMY/CHINA_ENEMY/GLA_ENEMY (Enums)**: Player side relationships

## Key Functions
### ScoreScreenInit
- Purpose: Initializes the score screen UI
- Calls: initSinglePlayer, initSkirmish, initLANMultiPlayer, initInternetMultiPlayer, initReplayMultiPlayer, initReplaySinglePlayer

### ScoreScreenShutdown
- Purpose: Shuts down the score screen UI
- Calls: None

### populateSideInfo
- Purpose: Populates score screen with statistics for a player side
- Calls: GadgetStaticTextSetText

### startNextCampaignGame
- Purpose: Starts the next game in a campaign
- Calls: TheShell->popImmediate, TheShell->hideShell, TheMessageStream->appendMessage

### ScoreScreenEnableControls
- Purpose: Enables/disables score screen controls
- Calls: winEnable

## Globals
- **parentID/buttonOkID/textEntryChatID/buttonEmoteID/chatBoxBorderID/buttonContinueID/buttonBuddiesID/buttonSaveReplayID (NameKeyType)**: Window IDs
- **parent/buttonOk/buttonContinue/textEntryChat/buttonEmote/chatBoxBorder/buttonBuddies/staticTextGameSaved (GameWindow**)**: UI window pointers
- **overidePlayerDisplayName (Bool)**: Flag for overriding player display names
- **listboxChatWindowScoreScreenID/listboxChatWindowScoreScreen (NameKeyType/GameWindow**)**: Chat window references
- **LastReplayFileName (std::string)**: Stores the last replay filename
- **canSaveReplay (Bool)**: Flag indicating if replay can be saved
- **s_needToFinishSinglePlayerInit/buttonIsFinishCampaign/s_blankLayout (Bool/WindowLayout**)**: Single-player init state
- **screenType (Int)**: Current score screen type
- **DontShowMainMenu/ReplayWasPressed (Bool)**: Global flags

## Dependencies
- Common: BattleHonors, GameEngine, GameLOD, GameState, GameSpyMiscPreferences, GlobalData, NameKeyGenerator, Player, PlayerList, PlayerTemplate, RandomValue, Recorder, ScoreKeeper, SkirmishBattleHonors, ThingFactory
- GameLogic: FPUControl, GameLogic, ScriptEngine, VictoryConditions
- GameClient: CDCheck, Display, GUICallbacks, WindowLayout, GameWindowManager, Gadget, GameText, MapUtil, Shell, KeyDefs, GadgetStaticText, GadgetTextEntry, GadgetPushButton, CampaignManager, GameWindowTransitions, VideoPlayer
- GameNetwork: PeerDefs, GameResultsThread, NetworkDefs, LANAPICallbacks, GameSpyOverlay,
