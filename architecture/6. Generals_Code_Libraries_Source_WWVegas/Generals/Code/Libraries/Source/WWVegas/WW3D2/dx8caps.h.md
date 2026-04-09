# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8caps.h

## Purpose
Header defining the DX8Caps class for querying Direct3D 8 hardware capabilities.

## Responsibilities
- Query and store Direct3D 8 hardware/software vertex processing capabilities
- Check support for texture formats, compression, shaders, and rendering features
- Provide accessors for shader versions, texture limits, and feature flags

## Key Types
- **DX8Caps (Class)**: Manages Direct3D 8 capability queries and feature detection

## Key Functions
### Compute_Caps
- Purpose: Initialize capability queries for given display/depth formats and device
- Calls: Init_Caps, Check_Texture_Format_Support, Check_Texture_Compression_Support, Check_Bumpmap_Support, Check_Shader_Support, Check_Maximum_Texture_Support, Vendor_Specific_Hacks

### Init_Caps
- Purpose: Query base D3D device capabilities
- Calls: Not inferable

### Check_Texture_Format_Support
- Purpose: Verify support for WW3D texture formats
- Calls: Not inferable

### Check_Texture_Compression_Support
- Purpose: Verify DXT compression support
- Calls: Not inferable

### Check_Bumpmap_Support
- Purpose: Verify bump mapping feature support
- Calls: Not inferable

### Check_Shader_Support
- Purpose: Verify vertex/pixel shader support and versions
- Calls: Not inferable

### Check_Maximum_Texture_Support
- Purpose: Verify maximum texture size support
- Calls: Not inferable

### Vendor_Specific_Hacks
- Purpose: Apply workarounds for vendor-specific D3D driver bugs
- Calls: Not inferable

## Globals
- **hwV
