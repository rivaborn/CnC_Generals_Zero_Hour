# Generals/Code/GameEngine/Source/GameClient/Drawable.cpp

## Purpose
Manages graphical "Drawables" in the game client, binding visual representations to game logic objects.

## Responsibilities
- Handles icon rendering (healing, battle plans, etc.)
- Manages drawable modules and their states
- Controls stealth visibility and opacity effects
- Processes network serialization (Xfer) for drawables
- Maintains health bars and condition indicators

## Key Types
- `DrawableIconInfo`: Manages icon states and timers
- `DrawableLocoInfo`: Tracks locomotion-related visual data
- `TintEnvelope`: Handles color tint transitions for effects
- `Drawable` (class): Core drawable entity with rendering logic

## Key Functions
### `drawableIconIndexToName`
- Purpose: Converts icon index to its string name
- Calls: None

### `drawableIconNameToIndex`
- Purpose: Converts icon name to its index
- Calls: `stricmp`

### `computeHealthRegion`
- Purpose: Calculates screen region for health bar display
- Calls: Not inferable (truncated in snippet)

### `TintEnvelope::update`
- Purpose: Updates tint envelope state for color transitions
- Calls: Vector3 math operations

## Globals
- `TheDrawableIconNames` (char*): Array of icon name strings
- `HEALING_ICON_DISPLAY_TIME` (UnsignedInt): Duration icons stay visible
- `DEFAULT_HEAL_ICON_WIDTH/HEIGHT` (UnsignedInt): Default icon dimensions
- `SICKLY_GREEN_POISONED_COLOR` (RGBColor): Poisoned unit color
- `RED_IRRADIATED_COLOR` (RGBColor): Irradiated unit color
- `FADE_RATE_EPSILON` (Real): Threshold for fade rate comparisons

## Dependencies
- Common: Audio, GameEngine, Player, ThingFactory
- GameLogic: Object, Weapon, Modules
- GameClient: Anim2D, Display, Image, ParticleSys
- External: Xfer (serialization), Matrix3D, Vector3
