# Generals/Code/Tools/WorldBuilder/include/FenceOptions.h

## Purpose
Defines the `FenceOptions` dialog class for configuring fence object properties in the WorldBuilder tool.

## Responsibilities
- Manages UI for fence object selection and spacing/offset settings
- Handles tree view navigation for object hierarchy
- Updates object properties based on user input
- Provides static accessors for current fence settings

## Key Types
- **FenceOptions (Class)**: Dialog for fence configuration in WorldBuilder
- **MapObject (Class)**: Reference type for map objects (defined elsewhere)
- **WorldHeightMapEdit (Class)**: Reference type for terrain editing (defined elsewhere)
- **(anonymous enum)**: Contains `NAME_MAX_LEN = 64` constant
- **(anonymous enum)**: Contains `IDD = IDD_FENCE_OPTIONS` dialog ID

## Key Functions
### FenceOptions::DoDataExchange
- Purpose: Handles DDX/DDV data exchange for dialog controls
- Calls: Not inferable (standard MFC method)

### FenceOptions::OnInitDialog
- Purpose: Initializes dialog controls and object tree view
- Calls: Not inferable

### FenceOptions::OnChangeFenceSpacingEdit
- Purpose: Handles changes to fence spacing edit control
- Calls: Not inferable

### FenceOptions::addObject
- Purpose: Adds an object to the tree view hierarchy
- Calls: Not inferable

### FenceOptions::findOrAdd
- Purpose: Finds or adds a tree node with given label
- Calls: Not inferable

### FenceOptions::setObjectTreeViewSelection
- Purpose: Sets the selection in the object tree view
- Calls: Not inferable

### FenceOptions::updateObjectOptions
- Purpose: Updates object options based on current selection
- Calls: Not inferable

### Fence
