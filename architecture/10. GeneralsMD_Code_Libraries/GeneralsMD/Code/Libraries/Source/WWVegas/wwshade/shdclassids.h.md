# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdclassids.h

## Purpose
Defines enumeration constants for shader class IDs used in the rendering pipeline.

## Responsibilities
- Declares shader definition class IDs (e.g., simple, glossmask, bumpmap).
- Declares shader implementation class IDs.
- Provides a header guard to prevent multiple inclusions.

## Key Types
- (anonymous enum) (Enum): Shader definition class IDs (e.g., `SHDDEF_CLASSID_SIMPLE`).
- SHDDEF_CLASSID_DUMMY (Enum): Dummy shader definition class ID.
- SHDDEF_CLASSID_SIMPLE (Enum): Simple shader definition class ID.
- SHDDEF_CLASSID_GLOSSMASK (Enum): Glossmask shader definition class ID.
- SHDDEF_CLASSID_BUMPSPEC (Enum): Bump-specular shader definition class ID.
- SHDDEF_CLASSID_BUMPDIFF (Enum): Bump-diffuse shader definition class ID.
- SHDDEF_CLASSID_CUBEMAP (Enum): Cubemap shader definition class ID.
- SHDDEF_CLASSID_LEGACYW3D (Enum): Legacy W3D shader definition class ID.
- SHDDEF_CLASSID_LAST (Enum): Last shader definition class ID (for iteration).
- (anonymous enum) (Enum): Shader implementation class IDs (e.g., `SHD_CLASSID_DUMMY`).
- SHD_CLASSID_DUMMY (Enum): Dummy shader implementation class ID.
- SHD_CLASSID_LAST (Enum): Last shader implementation class ID (for iteration).

## Key Functions
None.

## Globals
None.

## Dependencies
- None (header-only file).
