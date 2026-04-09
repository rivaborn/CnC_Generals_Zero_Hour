# GeneralsMD/Code/GameEngine/Source/Common/INI/INIVideo.cpp

## Purpose
Parses video-related entries from INI configuration files for the game.

## Responsibilities
- Parses video definitions from INI files
- Creates Video objects from parsed data
- Registers parsed videos with the video player system

## Key Types
- Video (struct): Represents a video asset with internal name and properties

## Key Functions
### parseVideoDefinition
- Purpose: Parses a video definition from an INI file and registers it with the video player
- Calls: ini->getNextToken(), ini->initFromINI(), TheVideoPlayer->getFieldParse(), TheVideoPlayer->addVideo()

## Globals
- TheVideoPlayer (VideoPlayer*): Global video player instance used to register parsed videos

## Dependencies
- INI.h: For INI parsing functionality
- GameClient/VideoPlayer.h: For VideoPlayer and Video types
- PreRTS.h: Required header for GameEngine files
