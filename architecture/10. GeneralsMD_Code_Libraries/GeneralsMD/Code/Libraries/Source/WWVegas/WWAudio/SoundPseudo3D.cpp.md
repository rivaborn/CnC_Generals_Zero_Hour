# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundPseudo3D.cpp

## Purpose
Implements pseudo-3D audio functionality for the game's sound system, handling volume and pan adjustments based on listener position.

## Responsibilities
- Manages pseudo-3D sound effects (volume and pan based on position)
- Updates sound properties per frame
- Handles MILES audio handle lifecycle
- Provides persistence factory for serialization

## Key Types
- **SoundPseudo3DClass (Class)**: Manages pseudo-3D audio effects with volume and pan calculations
- **MMSLockClass (Class)**: Used for thread synchronization (external)
- **Vector3 (Struct)**: 3D vector math (external)
- **Matrix3D (Class)**: 3D matrix operations (external)

## Key Functions
### Update_Pseudo_Volume(float distance)
- Purpose: Calculates and applies volume based on distance from listener
- Calls: `Determine_Real_Volume()`, `Get_DropOff_Radius()`, `Get_Max_Vol_Radius()`, `m_SoundHandle->Set_Sample_Volume()`

### Update_Pseudo_Volume()
- Purpose: Updates volume based on current sound/listener positions
- Calls: `Update_Pseudo_Volume(float)`

### Update_Pseudo_Pan()
- Purpose: Calculates and applies stereo pan based on sound position relative to listener
- Calls: `Matrix3D::Inverse_Transform_Vector()`, `WWMath::Atan2()`, `WWMath::Fast_Sin()`, `m_SoundHandle->Set_Sample_Pan()`

### On_Frame_Update(unsigned int milliseconds)
- Purpose: Frame update handler that refreshes pseudo-3D audio properties
- Calls: `Update_Pseudo_Volume()`, `Update_Pseudo_Pan()`, `Sound3DClass::On_Frame_Update()`

## Globals
- **_PseudoSound3DPersistFactory (SimplePersistFactoryClass)**: Persistence factory for SoundPseudo3DClass serialization

## Dependencies
- `soundpseudo3d.h`, `wwaudio.h`, `soundscene.h`, `utils.h`, `soundchunkids.h`, `persistfactory.h`, `soundhandle.h`
- MILES audio system (external)
- WWMath library (external)
- Vector3/Matrix3D math classes (external)
