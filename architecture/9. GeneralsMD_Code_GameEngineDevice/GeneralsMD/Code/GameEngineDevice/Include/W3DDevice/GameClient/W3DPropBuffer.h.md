# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DPropBuffer.h

## Purpose
Manages rendering of 3D props (objects) in the game world, handling addition, removal, positioning, and drawing.

## Responsibilities
- Maintains a buffer of props with their positions, visibility, and bounds
- Handles prop type definitions and instantiation
- Performs culling and visibility updates based on camera and shroud
- Supports serialization (snapshot system) for networking/saving

## Key Types
- **TProp (struct)**: Individual prop data (render object, position, visibility, bounds)
- **TPropType (struct)**: Prop type definition (render object, name, bounds)
- **W3DPropBuffer (class)**: Main prop buffer manager
- **RenderInfoClass (Class)**: External rendering context
- **LightClass (Class)**: External lighting system

## Key Functions
### `addProp`
- Purpose: Adds a new prop to the buffer
- Calls: Not inferable (implementation in .cpp)

### `removeProp`
- Purpose: Removes a prop by ID
- Calls: Not inferable

### `drawProps`
- Purpose: Renders all visible props
- Calls: `cull`, external rendering calls

### `cull`
- Purpose: Updates prop visibility based on camera and bounds
- Calls: Not inferable

### `notifyShroudChanged`
- Purpose: Invalidates visibility when shroud (fog of war) changes
- Calls: Not inferable

## Globals
- **MAX_PROPS (enum)**: Maximum prop count (4000)
- **MAX_TYPES (enum)**: Maximum prop type count (64)

## Dependencies
- `RenderObjClass`, `LightClass`, `W3DPropDrawModuleData`, `W3DShroudMaterialPass
