# Generals/Code/GameEngine/Source/Common/INI/INIAudioEventInfo.cpp

## Purpose
This file contains functions for parsing audio event, music track, and dialog event definitions from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parse audio event, music track, and dialog event definitions.
- Initialize `AudioEventInfo` objects with data from INI files.
- Handle specific fields like delay and pitch shift parsing.

## Key Types
- None

## Key Functions
### parseMusicTrackDefinition
- Purpose: Parses a music track definition from an INI file.
- Calls: 
  - `ini->getNextToken()`
  - `TheAudio->newAudioEventInfo(name)`
  - `TheAudio->findAudioEventInfo("DefaultMusicTrack")`
  - `TheAudio->addTrackName(name)`
  - `ini->initFromINI(track, track->getFieldParse())`

### parseAudioEventDefinition
- Purpose: Parses an audio event definition from an INI file.
- Calls: 
  - `ini->getNextToken()`
  - `TheAudio->newAudioEventInfo(name)`
  - `TheAudio->findAudioEventInfo("DefaultSoundEffect")`
  - `ini->initFromINI(track, track->getFieldParse())`

### parseDialogDefinition
- Purpose: Parses a dialog definition from an INI file.
- Calls: 
  - `ini->getNextToken()`
  - `TheAudio->newAudioEventInfo(name)`
  - `TheAudio->findAudioEventInfo("DefaultDialog")`
  - `ini->initFromINI(track, track->getFieldParse())`

### parseDelay
- Purpose: Parses delay values for an audio event.
- Calls: 
  - `ini->scanInt(ini->getNextToken())`
  - `DEBUG_ASSERTCRASH()`

### parsePitchShift
- Purpose: Parses pitch shift values for an audio event.
- Calls: 
  - `ini->scanReal(ini->getNextToken())`
  - `DEBUG_ASSERTCRASH()`

## Globals
- theAudioPriorityNames (char*[]): Array of audio priority names.
- theSoundTypeNames (char*[]): Array of sound type names.
- theAudioControlNames (char*[]): Array of audio control names.

## Dependencies
- Key includes:
  - "Common/INI.h"
  - "Common/GameAudio.h"
  - "Common/AudioEventInfo.h"
