# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalsys.h

## Purpose
Defines the decal system architecture for managing decals in the 3D engine, including decal generation, tracking, and pool management.

## Responsibilities
- Manages decal generation and tracking via `DecalSystemClass`
- Provides decal generator interface (`DecalGeneratorClass`)
- Implements fixed-pool decal management (`MultiFixedPoolDecalSystemClass`)
- Handles decal ID generation and mesh registration

## Key Types
- **DecalSystemClass (Class)**: Base class for decal system management
- **DecalGeneratorClass (Class)**: Encapsulates decal generation parameters and mesh tracking
- **MultiFixedPoolDecalSystemClass (Class)**: Manages multiple fixed-size decal pools
- **LogicalDecalClass (Class)**: Tracks meshes affected by a decal
- **LogicalDecalPoolClass (Class)**: Manages a pool of logical decals

## Key Functions
### DecalSystemClass::Lock_Decal_Generator
- Purpose: Creates and returns a decal generator
- Calls: `Generate_Decal_Id`

### DecalSystemClass::Unlock_Decal_Generator
- Purpose: Releases a decal generator back to the system
- Calls: None

### DecalGeneratorClass::Add_Mesh
- Purpose: Registers a mesh that generated decal polygons
- Calls: None

### MultiFixedPoolDecalSystemClass::Lock_Decal_Generator
- Purpose: Locks a decal generator and clears its slot
- Calls: `Clear_Decal_Slot`, `Generate_Decal_Id`

### MultiFixedPoolDecalSystemClass::find_logical_decal
- Purpose: Retrieves a logical decal by pool/slot ID or decal ID
- Calls: `decode_decal_id`

## Globals
- **DecalIDGenerator (uint32)**: Static counter for generating unique decal IDs

## Dependencies
- `always.h`, `matrix3d.h`, `matrix4.h`, `obbox.h`, `robjlist.h`, `matpass.h`, `projector.h`
- `ProjectorClass`, `MaterialPassClass`, `RenderObjClass`
