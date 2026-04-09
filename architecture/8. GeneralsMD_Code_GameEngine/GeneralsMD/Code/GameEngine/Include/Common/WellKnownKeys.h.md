# GeneralsMD/Code/GameEngine/Include/Common/WellKnownKeys.h

## Purpose
Defines well-known dictionary key constants used throughout the game engine for configuration and data lookup.

## Responsibilities
- Centralizes key definitions for team, player, map object, and world properties
- Provides documentation for each key's purpose and usage
- Uses a macro system to generate static name keys

## Key Types
- `StaticNameKey` (struct): Opaque handle for string keys in the game's dictionary system

## Key Functions
### `DEFINE_KEY`
- Purpose: Macro to declare or define a static name key
- Calls: `StaticNameKey` constructor (via macro expansion)

## Globals
- `TheKey_*` (const StaticNameKey): Global instances of each defined key (e.g., `TheKey_teamName`)

## Dependencies
- `Common/NameKeyGenerator.h`: For `StaticNameKey` and key generation macros
- Uses `INSTANTIATE_WELL_KNOWN_KEYS` define to control key instantiation
