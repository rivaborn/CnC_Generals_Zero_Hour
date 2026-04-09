# Generals/Code/Libraries/Source/WWVegas/WW3D2/hmorphanim.cpp

## Purpose
Handles morph animation data loading, saving, and interpolation for 3D models in the SAGE engine.

## Responsibilities
- Manages morph animation keys and their interpolation
- Imports/exports morph animations from/to text and binary formats
- Resolves pivot channels for morph targets
- Provides runtime morph interpolation (translation/orientation/transform)

## Key Types
- **TimeCodedMorphKeysClass**: Manages morph keyframes and their pose frame mappings
- **HMorphAnimClass**: Main morph animation controller with channel management
- **MorphKeyStruct**: Pair of morph frame and pose frame values

## Key Functions
### Build_List_From_String
- Purpose: Parses delimited strings into an array of StringClass objects
- Calls: strlen, strstr, strnicmp, W3DNEWARRAY

### Is_Number
- Purpose: Checks if a string contains only numeric characters
- Calls: None

### TimeCodedMorphKeysClass::Get_Morph_Info
- Purpose: Retrieves interpolated pose frames and fraction for a given morph frame
- Calls: get_index

### HMorphAnimClass::Import
- Purpose: Loads morph animation data from a text file
- Calls: Build_List_From_String, Is_Number, WW3DAssetManager::Get_Instance()

### HMorphAnimClass::Get_Transform
- Purpose: Computes interpolated transform matrix for a pivot at a given morph frame
- Calls: Get_Orientation, Get_Translation, Build_Matrix3D, Fast_Slerp

## Globals
- None

## Dependencies
- w3d_file.h, chunkio.h, assetmgr.h, htree.h, wwstring.h, textfile.h, simplevec.h
- WW3DAssetManager, ChunkLoadClass, ChunkSaveClass, HTreeClass, HAnimClass
- Vector3, Quaternion, Matrix3D, WWMath
