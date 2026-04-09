# Generals/Code/Libraries/Source/WWVegas/WW3D2/rddesc.h

## Purpose
Defines data structures for describing render devices and resolutions in the SAGE engine.

## Responsibilities
- Provides `ResolutionDescClass` to store display resolution parameters.
- Provides `RenderDeviceDescClass` to store detailed render device information.
- Manages dynamic string allocation/deallocation for device properties.
- Supports resolution enumeration and comparison operations.

## Key Types
- **ResolutionDescClass (Class)**: Stores width, height, bit depth, and refresh rate of a display resolution.
- **RenderDeviceDescClass (Class)**: Stores comprehensive render device metadata (name, vendor, driver info, hardware info) and associated resolutions.

## Key Functions
### `RenderDeviceDescClass::add_resolution`
- Purpose: Adds a unique resolution to the device's resolution list.
- Calls: `ResArray.Count()`, `ResArray[i]`, `ResArray.Add()`

### `RenderDeviceDescClass::operator=`
- Purpose: Assigns one device description to another, handling string duplication.
- Calls: `set_device_name`, `set_device_vendor`, `set_device_platform`, `set_driver_name`, `set_driver_vendor`, `set_driver_version`, `set_hardware_name`, `set_hardware_vendor`, `set_hardware_chipset`

## Globals
- None

## Dependencies
- `vector.h` (for `DynamicVectorClass`)
- `stdlib.h`, `string.h` (for memory/string operations)
- `WW3D`, `DX8Wrapper` (friend classes)
