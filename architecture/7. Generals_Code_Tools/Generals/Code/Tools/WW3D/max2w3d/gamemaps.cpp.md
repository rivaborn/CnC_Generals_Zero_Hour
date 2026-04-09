# Generals/Code/Tools/WW3D/max2w3d/gamemaps.cpp

## Purpose
Handles the GameMapsClass for 3D Studio Max plugin integration, managing texture map references and serialization.

## Responsibilities
- Defines GameMapsClass descriptor and post-load callback
- Implements reference management (assignment, cloning, notification)
- Handles saving/loading of texture map states to/from MAX files
- Provides class ID and factory methods

## Key Types
- **GameMapsPostLoad (Class)**: Post-load callback that does nothing (self-deleting)
- **GameMapsClassDesc (Class)**: Class descriptor for GameMapsClass registration
- **GameMapsClass (Class)**: Main class (defined elsewhere) for managing texture maps

## Key Functions
### GameMapsClass::ClassID
- Purpose: Returns the unique ClassID for GameMapsClass
- Calls: None

### GameMapsClass::AssignController
- Purpose: Assigns a controller to a sub-animation
- Calls: ReplaceReference, SubNumToRefNum

### GameMapsClass::NotifyRefChanged
- Purpose: Handles reference change notifications from MAX
- Calls: None

### GameMapsClass::Clone
- Purpose: Creates a deep copy of the GameMapsClass
- Calls: ReplaceReference, remap.CloneRef

### GameMapsClass::Save
- Purpose: Serializes GameMapsClass data to a MAX file
- Calls: isave->BeginChunk, isave->Write, isave->EndChunk

### GameMapsClass::Load
- Purpose: Deserializes GameMapsClass data from a MAX file
- Calls: iload->OpenChunk, iload->CurChunkID, iload->Read, iload->CloseChunk

## Globals
- **_GameMapsClassID (Class_ID)**: Unique identifier for GameMapsClass
- **_GameMapsCD (GameMapsClassDesc)**: Static instance of the class descriptor

## Dependencies
- Key includes: "gamemaps.h"
- External symbols: PostLoadCallback, ClassDesc, ILoad, ISave, Animatable, ReferenceTarget, RemapDir, RefTargetHandle, PartID, RefMessage, GetParamDim, GetParamName
