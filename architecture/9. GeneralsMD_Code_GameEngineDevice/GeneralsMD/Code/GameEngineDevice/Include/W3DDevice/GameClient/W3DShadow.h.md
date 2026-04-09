# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DShadow.h

## Purpose
Manages shadow rendering in the W3D (W3D) graphics subsystem for the game.

## Responsibilities
- Manages shadow casters and their rendering
- Controls shadow color and light positioning
- Handles shadow scene state and stencil masking
- Provides resource management for shadow rendering

## Key Types
- **W3DShadowManager (Class)**: Manages shadow rendering and configuration
- **Drawable (Class)**: Forward reference to renderable objects (not defined here)

## Key Functions
### W3DShadowManager::init
- Purpose: Initializes resources used by the shadow manager
- Calls: Not inferable

### W3DShadowManager::queueShadows
- Purpose: Flags the system to process shadows on the next render call
- Calls: Not inferable

### W3DShadowManager::addShadow
- Purpose: Adds a shadow caster to the rendering system
- Calls: Not inferable

### W3DShadowManager::RenderShadows
- Purpose: Renders all queued shadows
- Calls: Not inferable

### W3DShadowManager::ReleaseResources
- Purpose: Releases shadow rendering resources
- Calls: Not inferable

### W3DShadowManager::ReAcquireResources
- Purpose: Reacquires shadow rendering resources
- Calls: Not inferable

## Globals
- **TheW3DShadowManager (W3DShadowManager*)**: Global instance of the shadow manager

## Dependencies
- `matrix4.h` (Matrix4 class)
- `GameClient/Shadow.h` (Shadow class and related types)
- `Vector3` (from external source)
- `TimeOfDay` (enum from external source)
- `RenderObjClass` (from external source)
