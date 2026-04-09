# GeneralsMD/Code/GameEngine/Include/GameClient/Color.h

## Purpose
Defines color representation and utility functions for the game engine.

## Responsibilities
- Defines the `Color` type and related constants
- Provides functions to create and manipulate colors
- Supports color component extraction

## Key Types
- `GAME_COLOR_UNDEFINED` (Enum): Represents an undefined color (white with zero alpha)
- `Color` (Class): Typedef for `Int` representing a color value
- (anonymous enum) (Enum): Contains `GAME_COLOR_UNDEFINED`

## Key Functions
### `GameMakeColor`
- Purpose: Creates a color from RGBA components
- Calls: None

### `GameGetColorComponents`
- Purpose: Extracts RGBA components from a color
- Calls: None

### `GameGetColorComponentsReal`
- Purpose: Extracts RGBA components as floating-point values
- Calls: None

### `GameDarkenColor`
- Purpose: Darkens a color by a specified percentage
- Calls: None

## Globals
- None

## Dependencies
- `Lib/BaseType.h` (for `UnsignedByte`, `Int`, `Real` types)
