# GeneralsMD/Code/GameEngine/Include/GameClient/Anim2D.h

## Purpose
Defines classes and enums for 2D animation management in the game engine.

## Responsibilities
- Declares `Anim2DTemplate`, `Anim2D`, and `Anim2DCollection` classes for 2D animation.
- Defines animation modes and status flags.
- Provides INI parsing infrastructure for animation templates.
- Manages global animation collection singleton.

## Key Types
- **Image (Class)**: Forward reference to image resource.
- **Anim2DMode (Enum)**: Animation playback modes (invalid, once, loop, ping-pong, etc.).
- **Anim2DTemplate (Class)**: Template defining a 2D animation (frames, mode, etc.).
- **Anim2DStatus (Enum)**: Animation status flags (frozen, reversed, complete).
- **Anim2D (Class)**: Runtime animation instance with frame tracking and rendering.
- **Anim2DCollection (Class)**: System for managing animation templates and instances.

## Key Functions
### `Anim2D::draw(Int x, Int y)`
- Purpose: Draws current animation frame at specified position.
- Calls: `tryNextFrame()`

### `Anim2D::tryNextFrame()`
- Purpose: Advances animation frame if update conditions are met.
- Calls: Not inferable (implementation in .cpp).

### `Anim2DCollection::update()`
- Purpose: Updates all registered animation instances.
- Calls: Not inferable (implementation in .cpp).

## Globals
- **TheAnim2DCollection (Anim2DCollection*)**: Global animation collection singleton.

## Dependencies
- `Common/Snapshot.h` (for network synchronization)
- `INI` class (for template parsing)
- `MemoryPoolObject` (for memory management)
- `SubsystemInterface` (for system integration)
