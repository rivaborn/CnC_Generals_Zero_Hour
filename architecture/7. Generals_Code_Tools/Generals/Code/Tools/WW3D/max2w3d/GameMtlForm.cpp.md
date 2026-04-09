# Generals/Code/Tools/WW3D/max2w3d/GameMtlForm.cpp

## Purpose
Implements the `GameMtlFormClass` which manages a form for editing game materials in the Max2W3d tool.

## Responsibilities
- Manages the material being edited (`GameMtl`)
- Provides accessors for the material and its properties
- Handles form lifecycle (construction, deletion)
- Exposes material class ID

## Key Types
- `GameMtlFormClass` (Class): Form for editing game materials
- `GameMtl` (Type): The material being edited
- `IMtlParams` (Type): Material parameters interface

## Key Functions
### `GameMtlFormClass::GameMtlFormClass`
- Purpose: Constructor for the form class
- Calls: None

### `GameMtlFormClass::SetThing`
- Purpose: Sets the material being edited
- Calls: `assert`

### `GameMtlFormClass::GetThing`
- Purpose: Retrieves the material being edited
- Calls: None

### `GameMtlFormClass::DeleteThis`
- Purpose: Deletes the form instance
- Calls: `delete`

### `GameMtlFormClass::ClassID`
- Purpose: Returns the class ID of the material being edited
- Calls: None

### `GameMtlFormClass::SetTime`
- Purpose: Placeholder for time setting (no-op in base class)
- Calls: None

## Globals
- None

## Dependencies
- `GameMtlForm.h`
- `GameMtl.h`
- `ReferenceTarget` (from 3DS Max SDK)
- `IMtlParams` (from 3DS Max SDK)
- `MATERIAL_CLASS_ID`, `GameMaterialClassID` (constants)
