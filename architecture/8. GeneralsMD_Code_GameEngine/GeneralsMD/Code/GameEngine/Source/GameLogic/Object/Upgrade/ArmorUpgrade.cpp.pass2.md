# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ArmorUpgrade.cpp - Enhanced Analysis

## Architectural Role
This file implements the armor upgrade system, bridging the gap between upgrade modules and object behavior. It modifies object properties (armor flags, visuals) and ensures network synchronization via Xfer/CRC.

## Cross-References
### Incoming
- **UpgradeModule**: Base class that calls into `ArmorUpgrade` methods (crc, xfer, loadPostProcess).
- **BodyModule**: Used by `upgradeImplementation` to set armor flags.
- **Drawable**: Called for terrain decal changes (e.g., chemical suits).

### Outgoing
- **UpgradeModule**: Inherits and extends its functionality.
- **BodyModuleInterface**: Modifies object armor via `setArmorSetFlag`.
- **Drawable**: Updates visuals via `setTerrainDecal`.

## Design Patterns
- **Template Method**: `upgradeImplementation` defines a hook for armor-specific logic while delegating common upgrade behavior to `UpgradeModule`.
- **Strategy**: Armor upgrades are modular, allowing dynamic behavior changes (e.g., `ARMORSET_PLAYER_UPGRADE`).
- **Observer**: Implicitly notifies rendering/physics systems via `BodyModule` and `Drawable` updates.
