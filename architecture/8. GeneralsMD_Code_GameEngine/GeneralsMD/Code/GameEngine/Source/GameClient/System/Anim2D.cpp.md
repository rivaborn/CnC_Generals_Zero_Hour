# GeneralsMD/Code/GameEngine/Source/GameClient/System/Anim2D.cpp

## Purpose
Manages 2D animations in the game, including templates, instances, and their rendering/update logic.

## Responsibilities
- Defines `Anim2DTemplate` (animation definitions) and `Anim2D` (runtime instances)
- Handles animation modes (loop, ping-pong, etc.) and frame transitions
- Manages a global collection of animations (`Anim2DCollection`)
- Parses animation data from INI files

## Key Types
- **Anim2DTemplate (Class)**: Stores animation definition (images, modes, timing)
- **Anim2D (Class)**: Runtime animation instance with frame state and rendering
- **Anim2DCollection (Class)**: Manages global animation templates and instances
- **Anim2DMode (Enum)**: Defines animation playback modes (loop, ping-pong, etc.)

## Key Functions
### `Anim2D::tryNextFrame`
- Purpose: Advances animation to the next frame based on mode/timing.
- Calls: `setCurrentFrame`, `TheGameLogic->getFrame`

### `Anim2D::draw`
- Purpose: Renders the current animation frame at specified coordinates.
- Calls: `TheDisplay->drawImage`, `tryNextFrame`

### `Anim2DCollection::update`
- Purpose: Updates all registered animation instances.
- Calls: `Anim2D::tryNextFrame` for each instance

## Globals
- **TheAnim2DCollection (Anim2DCollection*)**: Global animation manager instance.

## Dependencies
- `Anim2D.h`, `Display.h`, `Image.h`, `GameLogic.h`
- `INI` class for parsing, `Xfer` for serialization
- `TheMappedImageCollection` (external image lookup)
