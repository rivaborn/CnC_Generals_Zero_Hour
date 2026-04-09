# Generals/Code/Libraries/Source/WWVegas/WW3D2/scene.h

## Purpose
Defines the core scene management classes for the WW3D rendering engine, including scene composition, rendering, and object iteration.

## Responsibilities
- Manages render objects in a 3D scene
- Provides scene iteration capabilities
- Handles scene rendering with fog, lighting, and polygon modes
- Supports object registration for frame updates, lighting, and release
- Implements save/load functionality for scene state

## Key Types
- **SceneClass (Class)**: Base class for managing a collection of render objects and scene rendering.
- **SceneIterator (Class)**: Abstract interface for iterating through render objects in a scene.
- **SimpleSceneClass (Class)**: Concrete implementation of SceneClass with basic visibility and LOD handling.
- **PolyRenderType (Enum)**: Defines polygon rendering modes (POINT, LINE, FILL).
- **ExtraPassPolyRenderType (Enum)**: Defines extra pass rendering modes for debugging.
- **RegType (Enum)**: Defines registration types for object processing (ON_FRAME_UPDATE, LIGHT, RELEASE).

## Key Functions
### SceneClass::Render
- Purpose: Renders the scene using the provided render info.
- Calls: Customized_Render, Pre_Render_Processing, Post_Render_Processing

### SimpleSceneClass::Visibility_Check
- Purpose: Determines visibility of render objects based on camera frustum.
- Calls: Not inferable (implementation not shown).

### SimpleSceneClass::Customized_Render
- Purpose: Handles the actual rendering of visible objects in the scene.
- Calls: Not inferable (implementation not shown).

## Globals
- None

## Dependencies
- **Includes**: "always.h", "refcount.h", "vector3.h", "robjlist.h", "wwdebug.h"
- **External Classes**: RenderObjClass, RenderInfoClass, CameraClass, ChunkLoadClass, ChunkSaveClass
- **External Types**: RefCountClass, Vector3, RefRenderObjListClass
