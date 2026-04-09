# GeneralsMD/Code/GameEngine/Source/GameClient/RadiusDecal.cpp

## Purpose
Manages circular decals (textures) projected onto the game world, used for visual effects like explosion marks or area indicators.

## Responsibilities
- Creates and updates radius decals based on templates
- Handles visibility rules (player-specific or global)
- Manages decal opacity and positioning
- Serializes decal data for save/load

## Key Types
- **RadiusDecalTemplate (Class)**: Defines decal properties (texture, style, opacity, etc.)
- **RadiusDecal (Class)**: Runtime instance of a decal with position and state
- **Shadow::ShadowTypeInfo (Struct)**: Shadow system configuration for decals

## Key Functions
### `RadiusDecalTemplate::createRadiusDecal`
- Purpose: Creates a decal instance from a template at a given position
- Calls: `TheProjectedShadowManager->addDecal`, `m_decal->setAngle`, `m_decal->setColor`, `m_decal->setPosition`

### `RadiusDecal::update`
- Purpose: Animates decal opacity over time (pulsing effect)
- Calls: `TheGameLogic->getFrame`, `TheGameLogic->getDrawIconUI`, `m_decal->setOpacity`

### `RadiusDecalTemplate::parseRadiusDecalTemplate`
- Purpose: Loads decal template data from INI files
- Calls: `ini->initFromINI`

## Globals
- **TheProjectedShadowManager**: Shadow system manager (external)
- **ThePlayerList**: Player management system (external)
- **TheGameLogic**: Game state and timing (external)

## Dependencies
- `Common/Player.h`, `Common/PlayerList.h`, `Common/Xfer.h`
- `GameClient/Shadow.h`, `GameLogic/GameLogic.h`
- `PreRTS.h` (engine precompiled header)
- Shadow system APIs (`addDecal`, `setOpacity`, etc.)
