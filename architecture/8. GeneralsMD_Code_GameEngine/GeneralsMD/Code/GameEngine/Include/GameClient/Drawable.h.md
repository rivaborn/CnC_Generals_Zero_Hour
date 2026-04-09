# GeneralsMD/Code/GameEngine/Include/GameClient/Drawable.h

## Purpose
Defines the `Drawable` class and related types for rendering game entities in the SAGE engine.

## Responsibilities
- Manages visual representation of game objects
- Handles animations, tints, stealth effects, and UI icons
- Provides physics-based transformations and sound management
- Supports network synchronization via snapshot system

## Key Types
- **Drawable (Class)**: Base class for all renderable game entities
- **DrawableIconType (Enum)**: Types of UI icons (health bars, veterancy, etc.)
- **TintEnvelope (Class)**: Manages color tint transitions (ADSR envelope)
- **StealthLookType (Enum)**: Different stealth visualization states
- **DrawableStatus (Enum)**: Bit flags for drawable state (shadows, reflections, etc.)

## Key Functions
### `draw(View *view)`
- Purpose: Renders the drawable to the given view
- Calls: `getTransformMatrix`, `getEffectiveOpacity`, module drawing functions

### `updateDrawable()`
- Purpose: Updates drawable state each frame
- Calls: `updateHiddenStatus`, `getColorTintEnvelope()->update`, module update functions

### `setModelConditionState(ModelConditionFlagType a)`
- Purpose: Updates drawable's visual state based on damage/condition
- Calls: `replaceModelConditionState`

## Globals
- **DRAWABLE_FRAMES_PER_FLASH (Int)**: Constant for flash animation timing

## Dependencies
- Common/AudioEventRTS.h, GameType.h, Thing.h
- GameClient/Color.h, DrawableInfo.h
- WWMath/Matrix3D.h
- ModuleFactory.h, Geometry.h, ModelState.h
