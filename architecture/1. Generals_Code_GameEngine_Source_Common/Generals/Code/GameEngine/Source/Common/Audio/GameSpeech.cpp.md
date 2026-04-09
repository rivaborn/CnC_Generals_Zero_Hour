# Generals/Code/GameEngine/Source/Common/Audio/GameSpeech.cpp

## Purpose
This file implements the audio speech system for Command & Conquer Generals, handling speech playback, management, and prioritization.

## Responsibilities
- Manages speech data and playback.
- Handles speaker creation and control.
- Manages speech queues and priorities.
- Provides interfaces for adding and canceling speeches.

## Key Types
- **Speech (Struct)**: Holds information about a line of dialog.
- **SpeechItem (Class)**: Internal structure for managing speech playback.
- **Flags (Enum)**: Flags for speech items, e.g., PAUSED.
- **Speaker (Class)**: Implements SpeakerInterface for controlling individual speakers.
- **SpeechManager (Class)**: Manages multiple speakers and speech data.

## Key Functions
### CreateSpeechInterface
- Purpose: Creates an instance of SpeechManager.
- Calls: None

### speechFromInfo
- Purpose: Populates a Speech struct from SpeechInfo.
- Calls: None

### getNextFilenameFromSpeech
- Purpose: Retrieves the filename for a given speech.
- Calls: None

## Globals
- None

## Dependencies
- **wpaudio/attributes.h**
- **wsys/File.h**
- **wsys/List.h**
- **wpaudio/Streamer.h**
- **wpaudio/Time.h**
- **wpaudio/Device.h**
- **Common/GameAudio.h**
- **Common/GameSpeech.h**
- **Common/INI.h**
