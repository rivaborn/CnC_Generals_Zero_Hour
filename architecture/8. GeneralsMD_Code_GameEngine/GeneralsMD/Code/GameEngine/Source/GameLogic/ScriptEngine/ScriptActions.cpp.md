# GeneralsMD/Code/GameEngine/Source/GameLogic/ScriptEngine/ScriptActions.cpp

## Purpose
Handles scripted actions in the game, executing commands from scripts to control game behavior.

## Responsibilities
- Execute scripted game actions (victory/defeat, object manipulation, AI commands)
- Manage game state changes via scripting (teams, players, upgrades)
- Handle UI and audio events triggered by scripts
- Process script action parameters and dispatch to appropriate handlers
- Maintain script execution context and state

## Key Types
- ScriptActions (Class): Main script action handler interface
- ScriptAction (Enum): Enumeration of all supported script actions
- SUBTITLE_DURATION (Enum): Subtitle duration constants

## Key Functions
### executeScriptAction
- Purpose: Dispatches script actions to their respective handlers
- Calls: doVictory, doDefeat, doQuickVictory, doLocalDefeat, doDebugMessage, doPlaySoundEffect, etc.

### doVictory/doDefeat/doQuickVictory/doLocalDefeat
- Purpose: Handle game end conditions (victory/defeat) with UI and state management
- Calls: closeWindows, TheGameLogic->closeWindows, doDisableInput, TheCampaignManager->SetVictorious, TheScriptEngine timers

### doPlaySoundEffect/doPlaySoundEffectAt
- Purpose: Play sound effects at specific locations or globally
- Calls: AudioEventRTS construction, TheAudio->addAudioEvent

### changeObjectPanelFlagForSingleObject
- Purpose: Modify object flags (enabled, powered, indestructible, etc.)
- Calls: obj->setScriptStatus, obj->setSelectable, body->setIndestructible

## Globals
- TheScriptActions (ScriptActionsInterface*): Global script actions interface instance
- m_messageWindow (GameWindow*): Current message window reference

## Dependencies
- Common: AudioAffect, GameAudio, Player, Team, Upgrade, etc.
- GameClient: Anim2D, CampaignManager, ControlBar, Eva, GameClient, etc.
- GameLogic: AI, Locomotor, Module classes, PartitionManager, ScriptEngine, etc.
- External: TheGlobalData, TheTerrainLogic, TheWindowManager, TheAudio, ThePlayerList, TheCampaignManager, TheVictoryConditions
