# Generals/Code/GameEngine/Source/GameClient/Drawable.cpp - Enhanced Analysis

## Architectural Role
This file bridges the game logic layer (GameLogic) and the rendering layer (W3D) by managing visual representations of game entities. It handles the synchronization between logical game state (e.g., health, stealth) and their graphical counterparts (e.g., health bars, tint effects).

## Cross-References
### Incoming
- **GameLogic/Object.h**: Uses `Drawable` as the visual component for game objects
- **GameClient/DrawModule.h**: Likely registers drawables for rendering passes
- **GameClient/Display.h**: Uses drawable coordinates for screen-space rendering

### Outgoing
- **Common/Xfer.h**: For network serialization of drawable state
- **GameLogic/Module/StealthUpdate.h**: Queries stealth state for visual effects
- **GameClient/Image.h**: Renders icons and health bars

## Design Patterns
- **Observer Pattern**: Drawables react to changes in game logic objects (e.g., health updates)
- **State Pattern**: `TintEnvelope` manages color transitions through discrete states (attack/decay/sustain)
- **Factory Pattern**: Icon creation via `TheDrawableIconNames` array (implicit in truncated code)

*Not inferable*: Exact relationship with W3D rendering pipeline (e.g., whether drawables are W3D objects or wrappers).
