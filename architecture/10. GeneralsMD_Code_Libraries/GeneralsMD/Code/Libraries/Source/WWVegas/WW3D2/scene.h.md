# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/scene.h

## Purpose
Defines the core scene management classes for the WW3D rendering engine, including scene hierarchy, render object management, and visibility handling.

## Responsibilities
- Manages 3D scene composition and rendering
- Provides iteration over render objects
- Handles scene-wide settings (fog, lighting, polygon modes)
- Supports object registration for frame updates/lights
- Implements save/load functionality for scene state

## Key Types
- **SceneClass (Class)**: Base class for scene management with render object handling
- **SimpleSceneClass (Class)**: Concrete implementation of SceneClass with visibility checks
- **SceneIterator (Class)**: Abstract iterator for traversing render objects
- **PolyRenderType (Enum)**: Defines polygon rendering modes (point/line/fill)
- **ExtraPassPolyRenderType (Enum)**: Controls second-pass debug rendering
- **RegType (Enum)**: Registration types for object processing (frame updates, lights, release)

## Key Functions
### SceneClass::Render
- Purpose: Renders the scene using provided render info
- Calls: Customized_Render, Pre_Render_Processing, Post_Render_Processing

### SimpleSceneClass::Visibility_Check
- Purpose: Determines which render objects are visible from the camera
- Calls: Not inferable (implementation in .cpp)

### SimpleSceneClass::Customized_Render
- Purpose: Handles actual rendering of visible objects
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- **Includes**: always.h, refcount.h, vector3.h, robjlist.h, wwdebug.h
- **External Classes**: RenderObjClass, RenderInfoClass, CameraClass, ChunkLoadClass, ChunkSaveClass
- **External Types**: RefCountClass, Vector3
