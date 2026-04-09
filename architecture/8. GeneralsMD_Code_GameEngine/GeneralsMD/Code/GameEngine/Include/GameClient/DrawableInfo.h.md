# GeneralsMD/Code/GameEngine/Include/GameClient/DrawableInfo.h

## Purpose
Defines a structure to link W3D render objects with game engine drawables, managing rendering flags and object references.

## Responsibilities
- Binds W3D render objects to game drawables
- Tracks shroud status via parent object ID
- Manages extra render flags (occlusion, transparency, etc.)
- Maintains pointers to drawable and ghost object instances

## Key Types
- **DrawableInfo (struct)**: Container for render-object-to-drawable binding data
- **ExtraRenderFlags (enum)**: Bitflags for render state (occlusion, transparency, etc.)

## Key Functions
### DrawableInfo/DrawableInfo
- Purpose: Default constructor initializing member variables
- Calls: None

## Globals
- None

## Dependencies
- `Common/GameType.h` (for `ObjectID`, `Int` types)
- Forward declarations: `Drawable`, `GhostObject`, `Object` classes
