# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ScoreScreen.cpp

## Purpose
Handles the score screen UI and logic after a game ends, displaying player statistics and managing post-game actions.

## Responsibilities
- Initialize and shutdown the score screen UI
- Populate score screen with player statistics (units built/destroyed, resources, etc.)
- Manage game transitions (next campaign mission, replay, etc.)
- Handle multiplayer-specific score screen logic (LAN, Internet, replay)
- Control UI elements (buttons, text, windows) based on game mode

## Key Types
- ScoreGather (Struct): Tracks player statistics (money, units, buildings)
- SCORESCREEN_SINGLEPLAYER/SCORESCREEN_SKIRMISH/SCORESCREEN_LAN/SCORESCREEN_INTERNET/SCORESCREEN_REPLAY (Enums): Score screen types
- USA_FRIEND/CHINA_FRIEND/GLA_FRIEND/USA_ENEMY/CHINA_ENEMY/GLA_ENEMY/MAX_RELATIONS (Enums): Player relations for side info

## Key Functions
### ScoreScreenInit
- Purpose: Initializes the score screen UI and sets up game-specific score screen
- Calls: initSinglePlayer, initSkirmish, initLANMultiPlayer, initInternetMultiPlayer, initReplayMultiPlayer, initReplaySinglePlayer

### ScoreScreenShutdown
- Purpose: Cleans up score screen resources
- Calls: Not inferable (truncated in source)

### populateSideInfo
- Purpose: Populates score screen with aggregated statistics for a player side
- Calls: GadgetStaticTextSetText, winSetEnabledTextColors, winHide

### startNextCampaignGame
- Purpose: Transitions to the next campaign mission
- Calls: TheShell->popImmediate, TheShell->hideShell, TheMessageStream->appendMessage

### ScoreScreenEnableControls
- Purpose: Enables/disables score screen controls based on game state
- Calls: winEnable

## Globals
- parentID/buttonOkID/textEntryChatID/buttonEmoteID/chatBoxBorderID/buttonContinueID/buttonBuddiesID/buttonSaveReplayID/backdropID (NameKeyType): UI element IDs
- parent/buttonOk/buttonContinue/textEntryChat/buttonEmote/chatBoxBorder/buttonBuddies/staticTextGameSaved/backdrop/challengePortrait/challengeRemarks/challengeWinLossText/gadgetParent (GameWindow*): UI element pointers
- overidePlayerDisplayName (Bool): Flag for overriding player display names
- listboxChatWindowScoreScreenID/listboxChatWindowScoreScreen/listboxAcademyWindowScoreScreenID/listboxAcademyWindowScoreScreen/staticTextAcademyTitleID/staticTextAcademyTitle (NameKeyType/GameWindow*): Chat and academy UI elements
- LastReplayFileName (std::string): Stores the last replay filename
- canSaveReplay (Bool): Flag indicating if replay can be saved
- s_needToFinishSinglePlayerInit/buttonIsFinishCampaign/s_blankLayout (static): Single player init state
- screenType (Int): Current score screen type
- DontShowMainMenu/g_playMusic/ReplayWasPressed (Bool): Global flags

## Dependencies
- Common: AudioAffect, AudioEventRTS, BattleHonors, GameEngine, GameState, Player, PlayerList, PlayerTemplate, Recorder, ScoreKeeper, SkirmishBattleHonors
- GameLogic: GameLogic, ScriptEngine, VictoryConditions
- GameClient: CDCheck, Display, GUICallbacks, WindowLayout, GameWindowManager, Gadget, GameText, MapUtil, Shell, KeyDefs
