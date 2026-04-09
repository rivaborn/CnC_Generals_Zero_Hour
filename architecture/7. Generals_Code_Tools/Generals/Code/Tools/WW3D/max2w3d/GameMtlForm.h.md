# Generals/Code/Tools/WW3D/max2w3d/GameMtlForm.h

## Purpose
Defines the `GameMtlFormClass` for material editing in the Max2W3d tool.

## Responsibilities
- Provides a form interface for editing `GameMtl` materials.
- Manages material pass-specific editing via `PassIndex`.
- Handles reference target management and deletion.
- Exposes material editor interface through `IMtlParams`.

## Key Types
- **GameMtlFormClass (Class)**: Material editing form for `GameMtl`.
- **GameMtl (Class)**: Reference to the material being edited (forward-declared).

## Key Functions
### `GameMtlFormClass(IMtlParams*, GameMtl*, int)`
- Purpose: Constructor initializing the form with material editor params, material, and pass index.
- Calls: None (constructor body not shown).

### `SetThing(ReferenceTarget*)`
- Purpose: Sets the reference target for the form.
- Calls: None (declaration only).

### `GetThing()`
- Purpose: Retrieves the current reference target.
- Calls: None (declaration only).

### `DeleteThis()`
- Purpose: Deletes the form instance.
- Calls: None (declaration only).

### `ClassID()`
- Purpose: Returns the class ID of the form.
- Calls: None (declaration only).

### `SetTime(TimeValue)`
- Purpose: Sets the time value for the form.
- Calls: None (declaration only).

## Globals
- **IParams (IMtlParams*)**: Interface to the material editor.
- **TheMtl (GameMtl*)**: Current material being edited.
- **PassIndex (int)**: Material pass index for editing.

## Dependencies
- `FormClass.h` (inheritance)
- `IMtlParams` (external
