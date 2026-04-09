# Generals/Code/GameEngine/Source/GameClient/Color.cpp

## Purpose
Handles color representation and manipulation in the game engine.

## Responsibilities
- Extracts color components (RGBA) from a color value
- Converts color components to floating-point values
- Darkens colors by a specified percentage

## Key Types
None

## Key Functions
### GameGetColorComponents
- Purpose: Extracts RGBA components from a color value.
- Calls: None

### GameGetColorComponentsReal
- Purpose: Extracts RGBA components as floating-point values (0.0 to 1.0).
- Calls: None

### GameDarkenColor
- Purpose: Darkens a color by a specified percentage.
- Calls: GameGetColorComponents, GameMakeColor

## Globals
None

## Dependencies
- "GameClient/Color.h" (for Color type and GameMakeColor function)
- "PreRTS.h" (included first in every GameEngine cpp file)
