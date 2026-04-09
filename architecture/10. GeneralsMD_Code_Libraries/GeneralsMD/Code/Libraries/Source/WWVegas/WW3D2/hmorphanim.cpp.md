# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmorphanim.cpp

## Purpose
Handles morph animation data loading, saving, and interpolation for 3D models in the SAGE engine.

## Responsibilities
- Manages morph animation keys and their interpolation
- Imports/exports morph animations from/to text and binary formats
- Resolves pivot channels for morph targets
- Provides runtime animation data access (translation/orientation)

## Key Types
- **TimeCodedMorphKeysClass**: Manages morph keyframes and their interpolation
- **HMorphAnimClass**: Main morph animation controller
- **MorphKeyStruct**: Pair of morph/pose frame values
- **W3dMorphAnimKeyStruct**: Binary format for morph keys

## Key Functions
### Build_List_From_String
- Purpose: Parses delimited strings into StringClass array
- Calls: strlen, strstr, strnicmp, W3DNEWARRAY

### Is_Number
- Purpose: Checks if string contains only numeric characters
- Calls: None

### TimeCodedMorphKeysClass::Get_Morph_Info
- Purpose: Gets interpolated pose frames for a given morph frame
- Calls: get_index

### HMorphAnimClass::Import
- Purpose: Loads morph animation from text file
- Calls: Build_List_From_String, Is_Number, WW3DAssetManager::Get_Instance()

### HMorphAnimClass::Get_Transform
- Purpose: Computes interpolated transform for a pivot at a given frame
- Calls: Get_Orientation, Get_Translation, Fast_Slerp, Build_Matrix3D

## Globals
- None

## Dependencies
- w3d_file.h, chunkio.h, assetmgr.h, htree.h, wwstring.h, textfile.h, simplevec.h
- WW3DAssetManager, StringClass, Vector3, Quaternion, Matrix3D, WWMath
