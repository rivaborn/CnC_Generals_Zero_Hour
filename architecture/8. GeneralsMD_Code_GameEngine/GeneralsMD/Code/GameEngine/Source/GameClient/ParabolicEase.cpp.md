# GeneralsMD/Code/GameEngine/Source/GameClient/ParabolicEase.cpp

## Purpose
Implements parabolic easing functions for smooth transitions in animations or interpolations.

## Responsibilities
- Provides parabolic easing calculations for ease-in and ease-out effects
- Validates input parameters and clamps out-of-range values
- Computes easing values based on configured ease-in/out times

## Key Types
- `ParabolicEase` (Class): Manages parabolic easing calculations
- `clamp` (Function template): Utility to clamp values within a range

## Key Functions
### `setEaseTimes`
- Purpose: Configures ease-in and ease-out times for the parabolic function
- Calls: `clamp`, `DEBUG_CRASH`

### `operator()`
- Purpose: Computes the eased value for a given parameter
- Calls: `clamp`, `DEBUG_CRASH`

## Globals
- None

## Dependencies
- `PreRTS.h`
- `GameClient/ParabolicEase.h`
- `DEBUG_CRASH` macro
- `Real` type (floating-point)
