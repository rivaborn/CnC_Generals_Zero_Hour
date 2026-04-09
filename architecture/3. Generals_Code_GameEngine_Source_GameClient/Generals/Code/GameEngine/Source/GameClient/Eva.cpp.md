# Generals/Code/GameEngine/Source/GameClient/Eva.cpp

## Purpose
Manages in-game voice announcements (EVA) triggered by game events.

## Responsibilities
- Loads and parses EVA event definitions from INI files
- Tracks game state to determine when announcements should play
- Plays announcements with appropriate timing and priority
- Manages announcement cooldowns and expiration

## Key Types
- **Eva (Class)**: Main EVA system controller
- **EvaCheckInfo (Class)**: Stores configuration for a specific EVA message type
- **EvaCheck (Class)**: Tracks individual EVA message instances and their state
- **EvaSideSounds (Struct)**: Maps player sides to associated sound files
- **EvaMessage (Enum)**: List of all possible EVA message types

## Key Functions
### `Eva::update()`
- Purpose: Main update loop that checks and plays EVA messages
- Calls: `isTimeForCheck`, `messageShouldPlay`, `playMessage`, `processPlayingMessages`

### `Eva::playMessage()`
- Purpose: Queues a new EVA message for playback
- Calls: `getEvaCheckInfo`

### `Eva::processPlayingMessages()`
- Purpose: Handles actual playback of queued EVA messages
- Calls: `m_evaSpeech.setEventName`, `m_evaSpeech.setPlayingHandle`

### `Eva::shouldPlayLowPower()`
- Purpose: Determines if low power warning should play
- Calls: `localPlayer->getEnergy()->hasSufficientPower()`

## Globals
- **TheEvaMessageNames (const char\*)**: Array mapping EVA message enums to string names
- **TheEva (Eva\*)**: Global instance of the EVA system

## Dependencies
- `GameClient/Eva.h`
- `Common/Player.h`, `Common/PlayerList.h`
- `GameLogic/GameLogic.h`
- INI parsing utilities (`INI::parse*`)
- Audio system (`TheAudio->addAudioEvent`)
