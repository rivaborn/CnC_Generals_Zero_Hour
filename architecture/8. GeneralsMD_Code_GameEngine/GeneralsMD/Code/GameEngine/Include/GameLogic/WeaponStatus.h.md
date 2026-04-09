# GeneralsMD/Code/GameEngine/Include/GameLogic/WeaponStatus.h

## Purpose
Defines an enum representing the possible states of a weapon in the game.

## Responsibilities
- Declares the `WeaponStatus` enum and its values.
- Provides a count of weapon states for iteration or array sizing.

## Key Types
- WeaponStatus (Enum): Represents the state of a weapon (e.g., ready, reloading, out of ammo).
- READY_TO_FIRE (Enum): Weapon is ready to fire.
- OUT_OF_AMMO (Enum): Weapon has no ammunition.
- BETWEEN_FIRING_SHOTS (Enum): Weapon is cooling down between shots.
- RELOADING_CLIP (Enum): Weapon is reloading a clip.
- PRE_ATTACK (Enum): Weapon is in pre-attack state.
- WEAPON_STATUS_COUNT (Enum): Count of weapon states (used for iteration/array sizing).

## Key Functions
None.

## Globals
None.

## Dependencies
- None (header-only, no includes or external symbols).
