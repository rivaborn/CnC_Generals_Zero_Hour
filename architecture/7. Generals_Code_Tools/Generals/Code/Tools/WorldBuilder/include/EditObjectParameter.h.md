# Generals/Code/Tools/WorldBuilder/include/EditObjectParameter.h

## Purpose
Header for the `EditObjectParameter` dialog class used in WorldBuilder to edit object parameters.

## Responsibilities
- Manages a tree view control for object parameters
- Provides methods to add objects and object lists to the tree
- Handles dialog initialization and user actions (OK/Cancel)
- Interfaces with `Parameter` and `ThingTemplate` data structures

## Key Types
- **EditObjectParameter (Class)**: Dialog for editing object parameters in WorldBuilder.
- **SidesList (Class)**: Forward-declared class for side management (not defined here).
- **(anonymous enum) (Enum)**: Contains `IDD` enum value for dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### `DoDataExchange`
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: Not inferable (DDX/DDV framework calls).

### `findOrAdd`
- Purpose: Finds or adds a tree node with the given label under a parent node.
- Calls: Not inferable.

### `addObject`
- Purpose: Adds a `ThingTemplate` object to the tree view.
- Calls: Not inferable.

### `addObjectLists`
- Purpose: Populates the tree view with object lists.
- Calls: Not inferable.

### `OnInitDialog`
- Purpose: Initializes the dialog and its controls.
- Calls: Not inferable.

### `OnOK`
- Purpose: Handles the OK button click event.
- Calls: Not inferable.

### `OnCancel`
- Purpose: Handles the Cancel button click event.
- Calls: Not inferable.

## Globals
- **m_parameter (Parameter**)**: Pointer to the parameter being edited.
- **m_objectTreeView (CTreeCtrl)**: Tree control for displaying object
