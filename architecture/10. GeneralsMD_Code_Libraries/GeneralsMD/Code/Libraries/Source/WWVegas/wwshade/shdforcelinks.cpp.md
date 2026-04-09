# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdforcelinks.cpp

## Purpose
Forces linking of shader classes that might otherwise be optimized out of the static library.

## Responsibilities
- Ensures critical shader classes remain linked
- Prevents dead code elimination for specific shaders
- Maintains shader availability for runtime use

## Key Types
None

## Key Functions
### SHD_Force_Links
- Purpose: Forces linking of shader classes that would otherwise be removed by linker optimization.
- Calls: FORCE_LINK (SimpleShader), FORCE_LINK (GlossMaskShader), FORCE_LINK (BumpSpecShader), FORCE_LINK (BumpDiffShader), FORCE_LINK (CubeMapShader), FORCE_LINK (LegacyW3DShader)

## Globals
None

## Dependencies
- shdforcelinks.h
- wwhack.h (for FORCE_LINK macro)
