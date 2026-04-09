# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DSmudge.h

## Purpose
Header for the W3DSmudgeManager class, managing particle effects (smudges) in the W3D rendering system.

## Responsibilities
- Manages particle groups and their rendering
- Handles resource acquisition/release for particles
- Tests hardware support for effects
- Maintains buffers for particle positions, colors, and sizes

## Key Types
- W3DSmudgeManager (Class): Manages particle effects rendering
- SmudgeGroupClass (Class): Forward reference to particle group
- Vector3 (Class): 3D vector type
- Vector4 (Class): 4D vector type
- TextureClass (Class): Texture handling
- RenderInfoClass (Class): Rendering information
- DX8IndexBufferClass (Class): DirectX 8 index buffer
- MAX_POINTS_PER_GROUP (Enum): Maximum particles per group (512)

## Key Functions
### W3DSmudgeManager::init
- Purpose: Initializes the smudge manager
- Calls: Not inferable

### W3DSmudgeManager::render
- Purpose: Renders particle effects
- Calls: Not inferable

### W3DSmudgeManager::ReleaseResources
- Purpose: Releases rendering resources
- Calls: Not inferable

### W3DSmudgeManager::ReAcquireResources
- Purpose: Reacquires rendering resources
- Calls: Not inferable

### W3DSmudgeManager::testHardwareSupport
- Purpose: Tests if hardware supports particle effects
- Calls: Not inferable

## Globals
- None

## Dependencies
- GameClient/Smudge.h
- sharebuf.h
- SmudgeGroupClass, Vector3, Vector4, TextureClass, RenderInfoClass,
