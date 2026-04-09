# GeneralsMD/Code/GameEngine/Include/GameClient/Eva.h

## Purpose
Defines the EVA (Electronic Versatile Assistant) system for in-game voice announcements and event notifications.

## Responsibilities
- Manages EVA message types and their conditions
- Handles timing and priority of voice announcements
- Processes game events to trigger appropriate messages
- Provides INI parsing for EVA configuration
- Mainages audio playback for EVA voice lines

## Key Types
- EvaMessage (Enum): enumerates all possible EVA announcement types
- EvaCheckInfo (Class): stores configuration for each EVA message type
- EvaCheck (Struct): tracks state of individual EVA message checks
- Eva (Class): main EVA subsystem controller
- EvaSideSounds (Struct): associates sounds with player sides

## Key Functions
### Eva::playMessage
- Purpose: Plays a specific EVA message if conditions are met
- Calls: AudioEventRTS playback, messageShouldPlay

### Eva::messageShouldPlay
- Purpose: Determines if a message should play based on conditions
- Calls: shouldPlayLowPower, shouldPlayGenericHandler

### Eva::processPlayingMessages
- Purpose: Manages currently playing EVA messages
- Calls: AudioEventRTS state checks

## Globals
- TheEvaMessageNames (const char*): array mapping EVA messages to names
- TheEva (Eva*): global EVA subsystem instance

## Dependencies
- Common/SubsystemInterface.h
- Common/AudioEventRTS.h
- Player, INI classes
- MemoryPoolObject, FieldParse, AsciiString types
- std::vector, Bool, UnsignedInt types
