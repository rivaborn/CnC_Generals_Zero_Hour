# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/textureloader.h

## Purpose
Header file defining texture loading and management system for the SAGE engine, including asynchronous loading tasks and Direct3D texture handling.

## Responsibilities
- Declares texture loader classes and task management structures
- Defines interfaces for texture loading operations (thumbnail, surface, background/foreground)
- Manages texture load tasks with priority and state tracking
- Provides synchronization mechanisms for multi-threaded texture loading

## Key Types
- **TextureLoader (Class)**: Main texture loading interface with static methods
- **TextureLoadTaskClass (Class)**: Base class for texture loading tasks
- **CubeTextureLoadTaskClass (Class)**: Specialized task for cube map textures
- **VolumeTextureLoadTaskClass (Class)**: Specialized task for volume textures
- **TextureLoadTaskListClass (Class)**: Double-linked list for task management
- **SynchronizedTextureLoadTaskListClass (Class)**: Thread-safe version of task list
- **TaskType (Enum)**: Task types (none, thumbnail, load)
- **PriorityType (Enum)**: Task priorities (low, high)
- **StateType (Enum)**: Task states (none, load begun, load mipmap, load complete, complete)

## Key Functions
### TextureLoader::Request_Background_Loading
- Purpose: Adds a texture loading task to be processed in background thread
- Calls: Not visible in header

### TextureLoader::Request_Foreground_Loading
- Purpose: Requests immediate texture loading on next main thread update
- Calls: Not visible in header

### TextureLoader::Update
- Purpose: Updates texture loading system and processes completed tasks
- Calls: Not visible in header

### TextureLoadTaskClass::Begin_Load
- Purpose: Begins the texture loading process
- Calls: Begin_Compressed_Load, Begin_Uncompressed_Load

### TextureLoadTaskClass::Load
- Purpose: Loads texture mipmaps
- Calls: Load_Compressed_Mipmap, Load_Uncompressed_Mipmap

## Globals
- **TextureLoader::TextureLoadSuspended (bool)**: Flag to suspend texture loading
- **TextureLoader::TextureInactiveOverrideTime (int)**: Time before inactive textures are unloaded

## Dependencies
- "texture.h" for texture base class definitions
- Direct3D 8 interfaces (IDirect3DTexture8, etc.)
- StringClass for filename handling
- Vector3 for HSV color shifting
- FastCriticalSectionClass for thread synchronization
