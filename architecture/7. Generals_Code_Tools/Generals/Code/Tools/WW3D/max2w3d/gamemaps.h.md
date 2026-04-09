# Generals/Code/Tools/WW3D/max2w3d/gamemaps.h

## Purpose
Defines classes for managing texture maps in the MAX plugin for Generals' W3D format.

## Responsibilities
- Define `TexmapSlotClass` for individual texture slots
- Define `GameMapsClass` for managing multiple texture slots
- Provide interface for MAX plugin to handle game material textures

## Key Types
- **TexmapSlotClass (Class)**: Represents a single texture slot with activation, amount, and map reference
- **GameMapsClass (Class)**: Manages a collection of texture slots for game materials

## Key Functions
### Get_Game_Maps_Desc
- Purpose: Returns ClassDesc for GameMapsClass
- Calls: None

## Globals
- None

## Dependencies
- `<Max.h>` for MAX SDK types
- `"stdmat.h"` for material definitions
- `ClassDesc`, `ReferenceTarget`, `Texmap`, `ShadeContext`, `MtlBase`, `Animatable`, `RefTargetHandle`, `TSTR`, `Class_ID`, `SClass_ID`, `TimeValue`, `Interval`, `Point3`, `RGBA`, `IOResult`, `ISave`, `ILoad`, `RemapDir`, `PartID`, `RefMessage`
