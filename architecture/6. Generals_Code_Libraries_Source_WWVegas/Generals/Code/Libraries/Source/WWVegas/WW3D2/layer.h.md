# Generals/Code/Libraries/Source/WWVegas/WW3D2/layer.h

## Purpose
Defines the LayerClass and related types for managing rendering layers in the W3D engine.

## Responsibilities
- Manages scene and camera references for rendering layers
- Provides layer creation, copying, and reference management
- Supports layer organization via ListNode and List patterns

## Key Types
- LayerClass (Class): Represents a rendering layer with scene/camera references
- LayerNodeClass (typedef): Node for LayerClass in linked list
- LayerListClass (typedef): List of LayerClass pointers
- SceneClass (forward declaration): Scene reference type
- CameraClass (forward declaration): Camera reference type

## Key Functions
### LayerClass::Set_Scene
- Purpose: Sets the scene reference with proper handling
- Calls: Not inferable

### LayerClass::Set_Camera
- Purpose: Sets the camera reference with proper handling
- Calls: Not inferable

### LayerClass::Set
- Purpose: Copies layer data from another LayerClass instance
- Calls: Not inferable

## Globals
- None

## Dependencies
- "always.h", "listnode.h", "vector3.h"
- SceneClass, CameraClass (forward declarations)
- Node, List templates (from listnode.h)
- Vector3 class
