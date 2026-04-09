# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8caps.cpp

## Purpose
Handles Direct3D 8 hardware/software capability detection and feature support checks for the game engine.

## Responsibilities
- Detects hardware/software vertex processing capabilities
- Checks support for texture formats, shaders, bump mapping, and compression
- Applies vendor-specific workarounds for known driver issues
- Initializes global capability flags used by the rendering system

## Key Types
- (anonymous enum) (Enum): Contains vendor IDs for NVIDIA and ATI
- VENDOR_ID_NVIDIA (Enum): NVIDIA vendor ID constant
- VENROD_ID_ATI (Enum): ATI vendor ID constant

## Key Functions
### Init_Caps
- Purpose: Initializes hardware/software vertex processing capabilities
- Calls: GetDeviceCaps

### Compute_Caps
- Purpose: Computes all supported rendering capabilities
- Calls: Init_Caps, Check_Texture_Format_Support, Check_Texture_Compression_Support, Check_Bumpmap_Support, Check_Shader_Support, Check_Maximum_Texture_Support, Vendor_Specific_Hacks

### Check_Bumpmap_Support
- Purpose: Determines bump mapping support from device caps
- Calls: None

### Check_Texture_Compression_Support
- Purpose: Checks for DXT texture compression support
- Calls: None

### Check_Texture_Format_Support
- Purpose: Verifies support for each WW3D texture format
- Calls: WW3DFormat_To_D3DFormat, CheckDeviceFormat

### Vendor_Specific_Hacks
- Purpose: Applies workarounds for known driver bugs
- Calls: None

## Globals
- hwVPCaps (D3DCAPS8):
