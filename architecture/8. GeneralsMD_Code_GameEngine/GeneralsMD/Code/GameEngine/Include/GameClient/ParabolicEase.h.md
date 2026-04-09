# GeneralsMD/Code/GameEngine/Include/GameClient/ParabolicEase.h

## Purpose
Provides a parabolic easing function for smooth transitions in animations or interpolations.

## Responsibilities
- Defines a parabolic easing curve with configurable ease-in and ease-out times.
- Calculates velocity and distance functions for smooth transitions.
- Evaluates the easing function at a given normalized time.

## Key Types
- **ParabolicEase (Class)**: Implements parabolic easing for smooth transitions.

## Key Functions
### ParabolicEase::ParabolicEase
- Purpose: Constructs a ParabolicEase object with optional ease-in and ease-out times.
- Calls: setEaseTimes

### ParabolicEase::setEaseTimes
- Purpose: Initializes the ease-in and ease-out times for the parabolic function.
- Calls: None

### ParabolicEase::operator()
- Purpose: Evaluates the easing function at a given normalized time.
- Calls: None

## Globals
- None

## Dependencies
- **Lib/BaseType.h**: For the `Real` type (floating-point number).
- **Not inferable**: External symbols or includes not explicitly listed.
