# GeneralsMD/Code/GameEngine/Source/GameClient/Credits.cpp - Enhanced Analysis

## Architectural Role
This file implements the credits system, which is part of the UI subsystem. It handles the loading, rendering, and scrolling of credits text during the credits sequence, interacting with the display and string management systems.

## Cross-References
### Incoming
- `INI::parseCredits` is called by the INI parsing system when loading credits definitions
- Likely invoked by the main game loop or sequence manager during credits playback

### Outgoing
- Uses `TheDisplayStringManager` for string resource management
- Depends on `TheDisplay` for screen dimensions and rendering context
- Relies on `TheGameText` for localized string lookup
- Uses `TheFontLibrary` indirectly through `DisplayString` objects

## Design Patterns
- **Singleton Pattern**: Global `TheCredits` instance provides centralized access to credits functionality
- **Strategy Pattern**: Different credit styles (title, position, normal, column) are handled through conditional logic in `draw()`
- **Observer Pattern**: Credits lines are updated and rendered based on global state (scroll position, timing)
