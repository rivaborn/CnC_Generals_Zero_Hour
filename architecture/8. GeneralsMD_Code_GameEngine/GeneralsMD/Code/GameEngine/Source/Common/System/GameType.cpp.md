# GeneralsMD/Code/GameEngine/Source/Common/System/GameType.cpp

## Purpose
Defines string arrays for time-of-day and weather type names used in the game.

## Responsibilities
- Provides human-readable names for time-of-day states
- Provides human-readable names for weather states
- Terminates arrays with NULL for iteration safety

## Key Types
None

## Key Functions
None

## Globals
- TimeOfDayNames (char*): Array of time-of-day state names ("NONE", "MORNING", etc.)
- WeatherNames (char*): Array of weather state names ("NORMAL", "SNOWY")

## Dependencies
- "PreRTS.h" (included first)
