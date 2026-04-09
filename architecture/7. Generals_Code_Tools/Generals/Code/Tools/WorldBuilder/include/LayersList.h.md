# Generals/Code/Tools/WorldBuilder/include/LayersList.h

## Purpose
Header file defining classes for managing map object layers in the WorldBuilder tool.

## Responsibilities
- Declares `LayersList` class for layer management UI
- Defines `Layer` struct and related container types
- Provides `CLLTreeCtrl` for right-click context menus
- Manages map object layering operations

## Key Types
- `Layer` (struct): Contains layer name, object list, and visibility flag
- `ListLayer` (typedef): Container for `Layer` objects
- `CLLTreeCtrl` (class): Custom tree control with right-click support
- `LayersList` (class): Main dialog for layer management

## Key Functions
### `LayersList::addMapObjectToLayersList`
- Purpose: Adds a map object to a specified layer
- Calls: `addMapObjectToLayer`, `findLayerNamed`

### `LayersList::removeMapObjectFromLayersList`
- Purpose: Removes a map object from its current layer
- Calls: `findMapObjectAndList`, `removeMapObjectFromLayer`

### `LayersList::updateUIFromList`
- Purpose: Synchronizes UI with current layer data
- Calls: Not inferable

## Globals
- `TheLayersList` (LayersList*): Global instance of the layer manager

## Dependencies
- `Common/AsciiString.h`
- MFC classes (`CTreeCtrl`, `CDialog`, etc.)
- STL containers (`list`, `string`)
