# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/layer.h

## Purpose
Defines the LayerClass and related types for managing rendering layers in the W3D engine.

## Responsibilities
- Declares LayerClass for scene/camera management
- Provides layer node and list types
- Exposes layer manipulation methods

## Key Types
- LayerClass (Class): Manages scene, camera, and rendering state for a layer
- LayerNodeClass (Class): Node type for LayerClass in linked lists
- LayerListClass (Class): List type for LayerClass pointers
- SceneClass (Class): Reference to scene (forward declared)
- CameraClass (Class): Reference to camera (forward declared)

## Key Functions
### LayerClass::Set_Scene
- Purpose: Sets the scene reference for this layer
- Calls: Not inferable

### LayerClass::Get_Scene
- Purpose: Returns the scene reference
- Calls: Not inferable

### LayerClass::Peek_Scene
- Purpose: Returns const scene reference
- Calls: Not inferable

### LayerClass::Set_Camera
- Purpose: Sets the camera reference for this layer
- Calls: Not inferable

### LayerClass::Get_Camera
- Purpose: Returns the camera reference
- Calls: Not inferable

### LayerClass::Peek_Camera
- Purpose: Returns const camera reference
- Calls: Not inferable

### LayerClass::Set
- Purpose: Copies layer state from another LayerClass
- Calls: Not inferable

## Globals
None

## Dependencies
- "always.h", "listnode.h", "vector3.h"
- SceneClass, CameraClass (forward declared)
