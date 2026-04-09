# Generals/Code/Tools/WW3D/max2w3d/skindata.h

## Purpose
Defines data structures for skinning mesh vertices to bones in 3D models, used in the Max2W3D toolchain.

## Responsibilities
- Manages vertex-bone influence data
- Handles vertex selection state
- Provides serialization for skin data
- Supports named selection sets

## Key Types
- **InfluenceStruct (struct)**: Stores bone influence data (indices and weights) for a single vertex
- **SkinDataClass (class)**: Container for skinning data, including vertex selection and influence info
- **(anonymous enum)**: Defines chunk IDs for serialization (FLAGS_CHUNK, VERT_SEL_CHUNK, NAMED_SEL_SETS_CHUNK, INFLUENCE_DATA_CHUNK)

## Key Functions
### InfluenceStruct::Set_Influence
- Purpose: Assigns a bone index to influence a vertex
- Calls: None

### SkinDataClass::Add_Influence
- Purpose: Applies bone influence to all currently selected vertices
- Calls: InfluenceStruct::Set_Influence

### SkinDataClass::Save/Load
- Purpose: Serialization methods for skin data
- Calls: Not inferable (external I/O interfaces)

## Globals
- None

## Dependencies
- Max.h (3DS Max SDK)
- namedsel.h (custom named selection set handling)
- LocalModData (base class for modifier data)
- BitArray, Tab (container classes)
- ILoad/ISave (serialization interfaces)
