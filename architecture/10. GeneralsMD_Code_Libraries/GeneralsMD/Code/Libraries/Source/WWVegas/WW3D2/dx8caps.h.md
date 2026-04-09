# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8caps.h

## Purpose
Defines the DX8Caps class for querying and managing Direct3D 8 hardware capabilities.

## Responsibilities
- Query and store Direct3D 8 device capabilities
- Identify GPU vendor and device type
- Check support for various rendering features (TnL, DXT compression, shaders, etc.)
- Log capability information for debugging

## Key Types
- **DX8Caps (Class)**: Main class for Direct3D 8 capability management
- **DriverVersionStatusType (Enum)**: Driver quality status (unknown/good/ok/bad)
- **VendorIdType (Enum)**: GPU vendor identifiers (NVIDIA, ATI, Intel, etc.)
- **DeviceTypeATI/3DLabs/NVidia/3Dfx/Matrox/PowerVR/S3/Intel (Enums)**: Device-specific identifiers for each vendor

## Key Functions
### DX8Caps(IDirect3D8*, const D3DCAPS8&, WW3DFormat, const D3DADAPTER_IDENTIFIER8&)
- Purpose: Constructor that initializes caps from D3D device and adapter info
- Calls: Compute_Caps

### Compute_Caps(WW3DFormat, const D3DADAPTER_IDENTIFIER8&)
- Purpose: Computes all supported features based on device capabilities
- Calls: Check_Texture_Format_Support, Check_Render_To_Texture_Support, Check_Depth_Stencil_Support, Check_Texture_Compression_Support, Check_Bumpmap_Support, Check_Shader_Support, Check_Maximum_Texture_Support, Check_Driver_Version_Status, Vendor_Specific_Hacks

### Support_TnL()
- Purpose: Returns whether transform and lighting is hardware-accelerated
- Calls: None

### Get_Vendor()
- Purpose: Returns the GPU vendor ID
- Calls: None

## Globals
- None

## Dependencies
- `always.h`, `ww3dformat.h`, `<d3d8.h>`
- Uses `StringClass`, `IDirect3D8`, `IDirect3DDevice8`, `D3DCAPS8`, `D3DADAPTER_IDENTIFIER8` from Direct3D 8 SDK
