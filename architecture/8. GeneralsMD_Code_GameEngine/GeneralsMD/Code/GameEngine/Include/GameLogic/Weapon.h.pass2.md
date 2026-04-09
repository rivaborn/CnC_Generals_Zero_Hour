# GeneralsMD/Code/GameEngine/Include/GameLogic/Weapon.h - Enhanced Analysis

## Architectural Role
This header defines the core weapon system architecture, bridging between object behavior and combat mechanics. It serves as the central interface for weapon templates, runtime weapon instances, and the weapon store subsystem, enabling damage calculation, projectile handling, and weapon bonuses.

## Cross-References
### Incoming
- **Object.h**: Uses Weapon for firing logic and weapon slot management
- **Projectile.h**: References Weapon for projectile creation and detonation
- **AI/Behavior.h**: Calls WeaponStore for template lookups during unit targeting
- **GameLogic/ObjectCreationList.h**: Uses WeaponStore for temporary weapon instantiation

### Outgoing
- **Damage.h**: Uses DamageType for weapon effects
- **AudioEventRTS.h**: References for weapon sound events
- **WWMath/Matrix3D.h**: For projectile positioning calculations
- **GameLogic/WeaponBonusConditionFlags.h**: For bonus condition evaluation

## Design Patterns
- **Template Method**: WeaponTemplate provides base firing logic while allowing specialization
- **Factory Method**: WeaponStore::allocateNewWeapon creates weapon instances
- **Observer**: WeaponStore tracks delayed damage via WeaponDelayedDamageInfo list

Rules followed. Output under 400 tokens.
