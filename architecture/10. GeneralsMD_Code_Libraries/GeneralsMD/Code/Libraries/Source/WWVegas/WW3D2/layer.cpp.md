# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/layer.cpp

## Purpose
Implements the `LayerClass` which manages rendering layers, including scene and camera references, and clear flags.

## Responsibilities
- Manages references to `SceneClass` and `CameraClass` objects
- Handles reference counting for scene and camera
- Provides accessors for scene and camera with reference management
- Maintains layer rendering settings (clear flags, color)

## Key Types
- `LayerClass` (Class): Manages a rendering layer with scene, camera, and clear settings
- `SceneClass*` (Pointer): Reference to the scene being rendered
- `CameraClass*` (Pointer): Reference to the camera used for rendering
- `Vector3` (Struct): Used for clear color

## Key Functions
### `LayerClass::LayerClass()`
- Purpose: Default constructor initializing members to null/false
- Calls: None

### `LayerClass::LayerClass(SceneClass*, CameraClass*, bool, bool, const Vector3&)`
- Purpose: Constructor with scene, camera, and clear settings
- Calls: `Add_Ref()` on scene and camera if not null

### `LayerClass::~LayerClass()`
- Purpose: Destructor releasing scene and camera references
- Calls: `Release_Ref()` on scene and camera

### `LayerClass::Set_Scene(SceneClass*)`
- Purpose: Sets the scene with reference management
- Calls: `Release_Ref()` on old scene, `Add_Ref()` on new scene

### `LayerClass::Get_Scene()`
- Purpose: Returns scene with reference increment
- Calls: `Add_Ref()` on scene

### `LayerClass::Peek_Scene()`
- Purpose: Returns scene without reference management
- Calls: None

### `LayerClass::Set_Camera(CameraClass*)`
- Purpose: Sets the camera with reference management
- Calls: `Release_Ref()` on old camera, `Add_Ref()` on new camera

### `LayerClass::Get_Camera()`
- Purpose: Returns camera with reference increment
- Calls: `Add_Ref()` on camera

### `LayerClass::Peek_Camera()`
- Purpose: Returns camera without reference management
- Calls: None

### `LayerClass::Set(const LayerClass&)`
- Purpose: Assignment-like operation copying layer settings
- Calls: `Set_Camera()`, `Set_Scene()`

## Globals
None

## Dependencies
- `layer.h`, `scene.h`, `camera.h`
- `SceneClass`, `CameraClass`, `Vector3` (external)
- Reference counting methods (`Add_Ref()`, `Release_Ref()`)
