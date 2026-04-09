# Generals/Code/Libraries/Source/WWVegas/WW3D2/layer.cpp

## Purpose
Implements the `LayerClass` which manages rendering layers, associating scenes and cameras with rendering settings.

## Responsibilities
- Manages scene and camera references with reference counting
- Controls layer-specific rendering flags (clear, clearZ, clear color)
- Provides accessor methods for scene and camera objects
- Handles layer state copying/assignment

## Key Types
- `LayerClass` (Class): Encapsulates a rendering layer with scene, camera, and rendering flags
- `SceneClass` (Class): Reference to the scene being rendered
- `CameraClass` (Class): Reference to the camera used for rendering
- `Vector3` (Struct): Used for clear color

## Key Functions
### `LayerClass::LayerClass()`
- Purpose: Default constructor initializing all members to null/false/black
- Calls: None

### `LayerClass::LayerClass(SceneClass*, CameraClass*, bool, bool, const Vector3&)`
- Purpose: Constructs a layer with specified scene, camera, and rendering flags
- Calls: `Add_Ref()` on scene and camera if not null

### `LayerClass::~LayerClass()`
- Purpose: Destructor releasing scene and camera references
- Calls: `Release_Ref()` on scene and camera if not null

### `LayerClass::Set_Scene(SceneClass*)`
- Purpose: Sets the scene for this layer with reference counting
- Calls: `Release_Ref()` on old scene, `Add_Ref()` on new scene

### `LayerClass::Set_Camera(CameraClass*)`
- Purpose: Sets the camera for this layer with reference counting
- Calls: `Release_Ref()` on old camera, `Add_Ref()` on new camera

### `LayerClass::Set(const LayerClass&)`
- Purpose: Copies layer state from another layer instance
- Calls: `Set_Camera()`, `Set_Scene()`

## Globals
None

## Dependencies
- `layer.h`, `scene.h`, `camera.h`
- `SceneClass`, `CameraClass`, `Vector3` (external)
- Reference counting methods (`Add_Ref()`, `Release_Ref()`)
