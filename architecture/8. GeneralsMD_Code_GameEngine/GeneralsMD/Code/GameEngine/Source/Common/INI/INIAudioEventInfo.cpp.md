# GeneralsMD/Code/GameEngine/Source/Common/INI/INIAudioEventInfo.cpp

## Purpose
Parses audio-related INI entries (MusicTrack, AudioEvent, DialogEvent) into AudioEventInfo objects.

## Responsibilities
- Parses INI definitions for audio events, music tracks, and dialogs
- Handles special fields like Delay and PitchShift
- Manages default audio event attributes
- Registers parsed audio events with the audio system

## Key Types
- **AudioEventInfo (Class)**: Stores audio event attributes (filename, volume, priority, etc.)
- **FieldParse (Struct)**: Defines INI field parsing rules

## Key Functions
### parseMusicTrackDefinition
- Purpose: Parses music track INI entries
- Calls: TheAudio->newAudioEventInfo, TheAudio->findAudioEventInfo, ini->initFromINI

### parseAudioEventDefinition
- Purpose: Parses audio event INI entries
- Calls: TheAudio->newAudioEventInfo, TheAudio->findAudioEventInfo, ini->initFromINI

### parseDialogDefinition
- Purpose: Parses dialog INI entries
- Calls: TheAudio->newAudioEventInfo, TheAudio->findAudioEventInfo, ini->initFromINI

### parseDelay
- Purpose: Parses delay range values
- Calls: ini->scanInt

### parsePitchShift
- Purpose: Parses pitch shift range values
- Calls: ini->scanReal

## Globals
- **theAudioPriorityNames (char**)**: Array of audio priority name strings
- **theSoundTypeNames (char**)**: Array of sound type name strings
- **theAudioControlNames (char**)**: Array of audio control name strings

## Dependencies
- INI.h, GameAudio.h, AudioEventInfo.h
- TheAudio (external audio system interface)
- INI class methods (parseAsciiString, parsePercentToReal, etc.)
