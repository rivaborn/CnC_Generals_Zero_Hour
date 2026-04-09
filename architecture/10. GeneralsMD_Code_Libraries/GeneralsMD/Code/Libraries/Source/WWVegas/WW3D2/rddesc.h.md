# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rddesc.h

## Purpose
Defines classes for describing render device capabilities and resolutions in the SAGE engine.

## Responsibilities
- Encapsulate render device metadata (vendor, driver, hardware info)
- Store supported resolutions and display modes
- Provide accessors for Direct3D 8 device capabilities

## Key Types
- **ResolutionDescClass (Class)**: Represents a display resolution (width, height, bit depth, refresh rate).
- **RenderDeviceDescClass (Class)**: Contains detailed info about a render device (name, vendor, driver, hardware, caps, resolutions).

## Key Functions
### `RenderDeviceDescClass::add_resolution`
- Purpose: Adds a unique resolution to the device's resolution list.
- Calls: `ResArray.Count()`, `ResArray.Add()`

### `RenderDeviceDescClass::operator=`
- Purpose: Assigns one device description to another.
- Calls: Multiple `set_*` methods, copies `Caps`, `AdapterIdentifier`, and `ResArray`.

## Globals
- None

## Dependencies
- `vector.h`, `wwstring.h`
- Direct3D 8 types (`d3d8types.h`, `d3d8caps.h`)
- `DynamicVectorClass`, `StringClass` (internal WW3D types)
