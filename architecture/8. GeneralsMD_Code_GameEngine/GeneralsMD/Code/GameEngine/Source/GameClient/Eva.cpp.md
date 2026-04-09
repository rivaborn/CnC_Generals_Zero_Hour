# GeneralsMD/Code/GameEngine/Source/GameClient/Eva.cpp

## Purpose
Manages the in-game AI assistant "EVA" that provides voice alerts to the player.

## Responsibilities
- Parses EVA event configurations from INI files
- Tracks game state to determine when alerts should play
- Plays voice alerts via audio system
- Manages alert cooldowns and priorities

## Key Types
- **Eva (Class)**: Main EVA system controller
- **EvaCheckInfo (Class)**: Configuration for a specific EVA message type
- **EvaCheck (Class)**: Runtime tracking for message playback timing
- **EvaSideSounds (Struct)**: Side-specific sound definitions for messages
- **EvaMessage (Enum)**: List of all possible EVA message types

## Key Functions
### parseSideSoundsList
- Purpose: Parses side-specific sound configurations from INI
- Calls: INI::initFromINI

### shouldPlayLowPower
- Purpose: Determines if low power alert should play
- Calls: Player::getEnergy()->hasSufficientPower()

### shouldPlayGenericHandler
- Purpose: Generic handler for most EVA messages
- Calls: None

### processPlayingMessages
- Purpose: Selects and plays highest priority pending EVA message
- Calls: TheAudio->addAudioEvent, m_evaSpeech.setPlayingHandle

## Globals
- **TheEvaMessageNames (const char**)**: Array mapping message enums to string names
- **TheEva (Eva**)**: Global EVA system instance

## Dependencies
- GameClient/Eva.h
- Common/Player.h, Common/PlayerList.h
- GameLogic/GameLogic.h
- INI parsing utilities
- Audio system (TheAudio)
