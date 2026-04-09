# Generals/Code/GameEngine/Source/GameClient/DrawGroupInfo.cpp

## Purpose
Defines the `DrawGroupInfo` class and its global instance for managing text rendering properties in the game client.

## Responsibilities
- Initializes default text rendering settings (font, color, offsets)
- Provides a global instance (`TheDrawGroupInfo`) for access to drawing configuration
- Encapsulates text display parameters (drop shadows, offsets, player color usage)

## Key Types
- `DrawGroupInfo` (Class): Holds configuration for text rendering (font, colors, offsets)
- `TheDrawGroupInfo` (Global pointer): Singleton instance of `DrawGroupInfo`

## Key Functions
### `DrawGroupInfo::DrawGroupInfo()`
- Purpose: Constructor initializing default text rendering parameters
- Calls: `GameMakeColor()` (external)

## Globals
- `TheDrawGroupInfo` (DrawGroupInfo*): Global singleton instance for drawing configuration

## Dependencies
- `PreRTS.h` (GameEngine precompiled header)
- `GameClient/DrawGroupInfo.h` (Header for this class)
- `GameMakeColor()` (External color utility function)
