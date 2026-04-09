# Generals/Code/Libraries/Source/WWVegas/WW3D2/textureloader.h

## Purpose
Header for texture loading and management in the SAGE engine, handling asynchronous texture loading tasks and Direct3D texture operations.

## Responsibilities
- Manages asynchronous texture loading via `TextureLoadTaskClass`
- Provides texture validation and format conversion utilities
- Handles Direct3D texture creation and surface loading
- Supports thumbnail generation and bumpmap creation
- Maintains texture loading priority system

## Key Types
- **TextureLoader (Class)**: Static class managing texture loading operations
- **TextureLoadTaskClass (Class)**: Represents a single texture loading task with state tracking
- **StringClass (Class)**: Used for filename handling (external)
- **IDirect3DTexture8 (Class)**: Direct3D texture interface (external)

## Key Functions
### TextureLoader::Add_Load_Task
- Purpose: Adds a texture loading task to the asynchronous loading system
- Calls: `Init_Load_Task`

### TextureLoader::Load_Surface_Immediate
- Purpose: Immediately loads a surface from file (synchronous)
- Calls: Not inferable (implementation in .cpp)

### TextureLoader::Update
- Purpose: Processes completed texture loading tasks
- Calls: Not inferable

### TextureLoadTaskClass::Begin_Texture_Load
- Purpose: Initiates texture loading (deferred if not on main thread)
- Calls: Not inferable

### TextureLoadTaskClass::Apply
- Purpose: Applies loaded texture data to the target texture
- Calls: Not inferable

## Globals
- **TextureLoadTaskClass::FreeTaskListHead (TextureLoadTaskClass*)**: Head of free task list for object pooling

## Dependencies
- `texture.h` (for `TextureClass`, `WW3DFormat`)
- Direct3D 8 interfaces (`
