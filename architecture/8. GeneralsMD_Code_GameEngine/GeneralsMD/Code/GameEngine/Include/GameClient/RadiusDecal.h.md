# GeneralsMD/Code/GameEngine/Include/GameClient/RadiusDecal.h

## Purpose
Defines classes for managing circular decals (shadows) on the game map, including their templates and runtime instances.

## Responsibilities
- Define `RadiusDecal` for rendering circular decals at world positions
- Define `RadiusDecalTemplate` for configuring decal appearance and behavior
- Support serialization via `Xfer` for network sync
- Provide parsing from INI files for modding

## Key Types
- **ShadowType (Enum)**: Type of shadow effect (not defined here)
- **Player (Class)**: Game player reference (not defined here)
- **Shadow (Class)**: Renderable decal object (not defined here)
- **RadiusDecal (Class)**: Runtime decal instance with position/opacity
- **RadiusDecalTemplate (Class)**: Configuration for decal appearance and behavior

## Key Functions
### RadiusDecal::xferRadiusDecal
- Purpose: Serialize/deserialize decal state for network sync
- Calls: `Xfer` methods

### RadiusDecalTemplate::createRadiusDecal
- Purpose: Create a decal instance from template at specified position
- Calls: Not inferable

### RadiusDecalTemplate::parseRadiusDecalTemplate
- Purpose: Parse decal template from INI file
- Calls: `INI` methods

## Globals
None

## Dependencies
- `Common/GameCommon.h`, `Common/GameType.h`, `GameClient/Color.h`
- `Xfer`, `INI`, `Coord3D`, `AsciiString`, `Bool`, `Real`, `UnsignedInt`
