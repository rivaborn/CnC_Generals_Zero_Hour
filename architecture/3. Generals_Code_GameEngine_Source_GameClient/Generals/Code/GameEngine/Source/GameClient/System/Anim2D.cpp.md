# Generals/Code/GameEngine/Source/GameClient/System/Anim2D.cpp

## Purpose
Manages 2D animations in the game, including templates, instances, and their rendering/update logic.

## Responsibilities
- Defines `Anim2DTemplate` for animation definitions (frames, modes, timing)
- Implements `Anim2D` for runtime animation instances
- Provides `Anim2DCollection` to manage templates and instances globally
- Handles INI parsing for animation data
- Supports network synchronization via Xfer

## Key Types
- **Anim2DTemplate (Class)**: Holds animation definition (images, mode, timing)
- **Anim2D (Class)**: Runtime animation instance with frame management
- **Anim2DCollection (Class)**: Global manager for templates/instances
- **Anim2DMode (Enum)**: Animation playback modes (loop, ping-pong, etc.)

## Key Functions
### `Anim2DTemplate::parseNumImages`
- Purpose: Allocates image array based on INI data
- Calls: None (direct)

### `Anim2D::tryNextFrame`
- Purpose: Advances animation frame based on mode/timing
- Calls: `setCurrentFrame`, `BitTest`, `TheGameLogic->getFrame`

### `Anim2DCollection::update`
- Purpose: Updates all registered animation instances
- Calls: `Anim2D::tryNextFrame`

### `Anim2D::draw`
- Purpose: Renders current animation frame
- Calls: `TheDisplay->drawImage`, `tryNextFrame`

## Globals
- **TheAnim2DCollection (Anim2DCollection*)**: Global animation manager instance

## Dependencies
- `Anim2D.h`, `Display.h`, `Image.h`, `GameLogic.h`
- `INI`, `Xfer`, `RandomValue` classes
- `TheMappedImageCollection`, `TheGameLogic`, `TheDisplay` globals
