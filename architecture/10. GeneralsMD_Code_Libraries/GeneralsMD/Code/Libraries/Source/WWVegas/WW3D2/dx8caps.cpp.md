# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8caps.cpp

## Purpose
Handles DirectX 8 hardware capability detection and vendor-specific workarounds for the SAGE engine.

## Responsibilities
- Detects GPU vendor/device and their capabilities
- Applies vendor-specific driver workarounds
- Logs capability information
- Validates display formats

## Key Types
- `DX8Caps` (Class): Main capability detection class
- `VendorIdType` (Enum): GPU vendor identifiers
- `DeviceTypeNVidia`/`DeviceTypeATI` etc. (Enums): Device-specific identifiers

## Key Functions
### `Define_Vendor`
- Purpose: Maps vendor IDs to vendor enum values
- Calls: None

### `Check_Depth_Stencil_Support`
- Purpose: Tests depth/stencil format compatibility
- Calls: `Direct3D->CheckDeviceFormat`, `WW3DFormat_To_D3DFormat`, `WW3DZFormat_To_D3DFormat`

### `Vendor_Specific_Hacks`
- Purpose: Applies vendor-specific driver workarounds
- Calls: None

### `Check_Driver_Version_Status`
- Purpose: Evaluates driver version quality
- Calls: `stricmp`

## Globals
- `CapsWorkString` (StringClass): Temporary string buffer
- `VendorNames` (const char*): Vendor name lookup table
- `DeviceNamesNVidia`/`DeviceNamesATI` etc. (const char[]): Device name lookup tables

## Dependencies
- `dx8caps.h`, `dx8wrapper.h`, `formconv.h`
- DirectX 8 headers (`d3d8.h` implied)
- Windows API (`windows.h`, `mmsystem.h`)
