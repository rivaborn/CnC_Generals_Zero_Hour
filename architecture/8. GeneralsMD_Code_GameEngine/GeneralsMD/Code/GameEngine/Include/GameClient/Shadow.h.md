# GeneralsMD/Code/GameEngine/Include/GameClient/Shadow.h

## Purpose
Defines shadow types, interfaces, and management for rendering shadows and decals in the game engine.

## Responsibilities
- Declares shadow types and their properties
- Defines the base `Shadow` class interface
- Provides `ProjectedShadowManager` for decal management
- Includes utility functions for shadow manipulation

## Key Types
- **ShadowType (Enum)**: Shadow rendering modes (decal, volume, projection, etc.)
- **Shadow::ShadowTypeInfo (Struct)**: Shadow configuration (name, type, size, offsets)
- **Shadow (Class)**: Base interface for shadow objects
- **ProjectedShadowManager (Class)**: Manages projected shadows and decals

## Key Functions
### `Shadow::setOpacity`
- Purpose: Adjusts shadow decal opacity based on type
- Calls: None (inline)

### `Shadow::setColor`
- Purpose: Sets ARGB color for shadow decals
- Calls: None (inline)

### `ProjectedShadowManager::addDecal`
- Purpose: Adds a decal (with or without object binding)
- Calls: None (pure virtual)

## Globals
- **TheProjectedShadowManager (ProjectedShadowManager*)**: Global manager instance

## Dependencies
- `RenderObjClass`, `RenderCost`, `Drawable` (forward declarations)
- `Color`, `Real`, `Bool`, `UnsignedInt` (types)
- `REAL_TO_INT` (macro)
