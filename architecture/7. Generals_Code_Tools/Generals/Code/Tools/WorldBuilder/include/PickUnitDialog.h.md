# Generals/Code/Tools/WorldBuilder/include/PickUnitDialog.h

## Purpose
Header for dialog classes used to select or replace units in the WorldBuilder editor.

## Responsibilities
- Define `PickUnitDialog` and `ReplaceUnitDialog` classes for unit selection.
- Manage tree view display of available units.
- Filter units by type and faction.
- Handle user selection and return picked unit data.

## Key Types
- **MapObject (Class)**: Not inferable.
- **ThingTemplate (Class)**: Not inferable.
- **PickUnitDialog (Class)**: Dialog for picking units from a tree view.
- **(anonymous enum)**: Contains `NAME_MAX_LEN = 64`.
- **NAME_MAX_LEN (Enum)**: Max length for object name buffer.
- **(anonymous enum)**: Contains `IDD = IDD_PICKUNIT`.
- **IDD (Enum)**: Dialog resource ID for `PickUnitDialog`.
- **ReplaceUnitDialog (Class)**: Dialog for replacing missing units.
- **(anonymous enum)**: Contains `IDD = IDD_REPLACEUNIT`.
- **IDD (Enum)**: Dialog resource ID for `ReplaceUnitDialog`.

## Key Functions
### `addObject`
- Purpose: Adds a map object to the tree view under a parent node.
- Calls: `findOrAdd`

### `findOrAdd`
- Purpose: Finds or creates a tree node with the given label.
- Calls: None

### `PickUnitDialog::PickUnitDialog`
- Purpose: Constructs the dialog with optional parent and resource ID.
- Calls: None

### `DoDataExchange`
- Purpose: Handles data exchange for the dialog.
- Calls: None

### `OnNotify`
- Purpose: Processes notifications from the tree view.
- Calls: None

### `OnInitDialog`
- Purpose: Initializes the dialog and populates the tree view.
- Calls: `addObject`,
