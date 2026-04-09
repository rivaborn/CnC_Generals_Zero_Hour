# Generals/Code/Tools/WW3D/max2w3d/GameMtlTextureDlg.h

## Purpose
Defines the `GameMtlTextureDlg` class for managing texture-related material properties in the Max2W3D tool.

## Responsibilities
- Manages UI dialog for texture stages (0 and 1)
- Handles texture property controls (frames, rates, clamping, etc.)
- Updates and enables/disables UI elements based on state
- Provides activation/reload functionality for the dialog

## Key Types
- **GameMtl (Class)**: Base material class (external)
- **GameMtlTextureDlg (Class)**: Dialog for texture stage properties
- **GameMtlFormClass (Class)**: Base form class (external)

## Key Functions
### GameMtlTextureDlg()
- Purpose: Constructor for the texture dialog.
- Calls: Not inferable.

### ~GameMtlTextureDlg()
- Purpose: Destructor for the texture dialog.
- Calls: Not inferable.

### Dialog_Proc()
- Purpose: Handles Windows messages for the dialog.
- Calls: Not inferable.

### ActivateDlg()
- Purpose: Activates or deactivates the dialog.
- Calls: Not inferable.

### ReloadDialog()
- Purpose: Reloads the dialog contents.
- Calls: Not inferable.

### Enable_Stage()
- Purpose: Enables/disables controls for a specific texture stage.
- Calls: Not inferable.

### Update_Texture_Buttons()
- Purpose: Updates the state of texture-related buttons.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `<Max.h>` (3ds Max SDK)
- `GameMtlForm.h` (local header)
- `ISpinnerControl`, `ICustButton` (3ds Max UI controls)
- `IMtlParams` (3ds
