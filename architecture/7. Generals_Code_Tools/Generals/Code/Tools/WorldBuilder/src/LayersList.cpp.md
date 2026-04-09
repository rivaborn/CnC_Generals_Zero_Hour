# Generals/Code/Tools/WorldBuilder/src/LayersList.cpp

## Purpose
Manages the layers system in WorldBuilder, allowing organization and visibility control of map objects.

## Responsibilities
- Maintains a hierarchical list of layers and objects
- Handles layer creation, deletion, and merging
- Controls object visibility via layer toggling
- Provides UI for layer management via tree control

## Key Types
- `CLLTreeCtrl` (Class): Custom tree control for layer display
- `LayersList` (Class): Main layer management dialog
- `Layer` (Struct): Represents a layer with name and visibility state
- `ListLayer` (Type): Container for layers
- `ListMapObjectPtrIt` (Type): Iterator for map objects in a layer

## Key Functions
### `CLLTreeCtrl::buildMoveMenu`
- Purpose: Builds a context menu for moving items between layers
- Calls: None

### `LayersList::addMapObjectToLayersList`
- Purpose: Adds a map object to a specified layer
- Calls: `findLayerNamed`, `addLayerNamed`, `addMapObjectToLayer`

### `LayersList::mergeLayerInto`
- Purpose: Merges one layer into another
- Calls: `changeMapObjectLayer`, `findTreeLayerNamed`

### `LayersList::updateUIFromList`
- Purpose: Updates the tree control to reflect current layer state
- Calls: None

### `LayersList::OnHideShowLayer`
- Purpose: Toggles layer visibility and updates object rendering
- Calls: `CWorldBuilderDoc::GetActiveDoc`, `invalObject`

## Globals
- `newLayerNum` (int): Counter for generating new layer names
- `TheLayersList` (LayersList*): Global pointer to the layers list instance
- `TheDefaultLayerName` (string): Name of the default layer
- `TheDefaultNewLayerName` (string): Template for new layer names
- `TheUnmutableDefaultLayerName` (const string): Constant default layer name

## Dependencies
- `StdAfx.h`, `Common/STLTypedefs.h`, `Resource.h`, `LayersList.h`
- `Common/Dict.h`, `Common/MapObject.h`, `Common/WellKnownKeys.h`
- `PointerTool.h`, `WorldBuilderDoc.h`
- MFC classes (`CDialog`, `CTreeCtrl`, `CMenu`)
- `MapObject` class methods
- Windows API (`LoadIcon`, `TreeView_EndEditLabelNow`)
