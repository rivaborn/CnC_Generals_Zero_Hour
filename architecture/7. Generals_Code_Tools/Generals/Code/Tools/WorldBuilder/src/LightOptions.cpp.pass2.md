# Generals/Code/Tools/WorldBuilder/src/LightOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for light object editing in WorldBuilder, bridging MFC dialog handling with the game's property system. It demonstrates the tool's separation of concerns between UI presentation and underlying data model.

## Cross-References
### Incoming
- `GlobalLightOptions.cpp` calls `LightOptions::update` to synchronize global and object-specific light settings
- `WbView3D.cpp` likely triggers `LightOptions::update` when selection changes

### Outgoing
- Directly manipulates `MapObject` properties via `Dict` interface
- Triggers view invalidation through `WbView3D::invalObjectInView`
- Uses `TheKey_*` constants from `Common/WellKnownKeys.h`

## Design Patterns
- **Observer Pattern**: The dialog observes selection changes (via external triggers) and updates accordingly
- **Property Bag Pattern**: Uses `Dict` for late-bound property access, enabling modding flexibility
- **Mediator Pattern**: Coordinates between UI controls and the underlying `MapObject` model

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns in this component.
