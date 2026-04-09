# Generals/Code/Libraries/Source/WWVegas/WWLib/iostruct.h

## Purpose
Defines basic I/O structures for vector and quaternion data used in chunk reading/writing.

## Responsibilities
- Declares fixed-size vector structures (2D, 3D, 4D)
- Defines quaternion structure for rotation data
- Provides stable binary layout for serialization

## Key Types
- **IOVector2Struct (struct)**: 2D vector with X/Y float32 components
- **IOVector3Struct (struct)**: 3D vector with X/Y/Z float32 components
- **IOVector4Struct (struct)**: 4D vector with X/Y/Z/W float32 components
- **IOQuaternionStruct (struct)**: Quaternion with 4 float32 components

## Key Functions
None

## Globals
None

## Dependencies
- `bittype.h` (for float32 definition)
