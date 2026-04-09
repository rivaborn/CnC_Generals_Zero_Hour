# GeneralsMD/Code/GameEngine/Source/GameClient/Color.cpp

## Purpose
Manages color representations and conversions in the game engine.

## Responsibilities
- Extracts RGB/alpha components from a color value
- Converts color components to floating-point values
- Darkens colors by a specified percentage

## Key Types
None

## Key Functions
### GameGetColorComponents
- Purpose: Extracts RGB/alpha components from a color value
- Calls: None

### GameGetColorComponentsReal
- Purpose: Converts color components to floating-point values
- Calls: None

### GameDarkenColor
- Purpose: Darkens a color by a specified percentage
- Calls: GameGetColorComponents, GameMakeColor

## Globals
None

## Dependencies
- Key includes: "PreRTS.h", "GameClient/Color.h"
- External symbols: GameMakeColor (used but not defined here)
