# GeneralsMD/Code/GameEngine/Source/GameClient/Drawable.cpp

## Purpose
Handles graphical representation of game entities (Drawables) and their interactions with the game world.

## Responsibilities
- Manages drawable icons, animations, and visual effects
- Handles stealth, opacity, and tinting effects
- Manages ambient sounds for drawables
- Serialization/deserialization of drawable state
- Health bar and status icon rendering

## Key Types
- `DrawableIconInfo` (Struct): Manages icon display state and timing
- `DrawableLocoInfo` (Struct): Tracks locomotion-related visual data
- `TintEnvelope` (Class): Handles color tinting transitions for drawables
- `Drawable` (Class): Base class for all drawable game entities

## Key Functions
### `getNoSoundMarker`
- Purpose: Creates a marker for "no sound" ambient sound state
- Calls: `newInstance`

### `drawableIconIndexToName`
- Purpose: Converts icon index to its string name
- Calls: None

### `drawableIconNameToIndex`
- Purpose: Converts icon name to its index
- Calls: `stricmp`

### `computeHealthRegion`
- Purpose: Calculates screen region for health bar display
- Calls: Not inferable from snippet

## Globals
- `TheDrawableIconNames` (Array): List of all drawable icon names
- `HEALING_ICON_DISPLAY_TIME` (UnsignedInt): Duration to show healing icons
- `DEFAULT_HEAL_ICON_WIDTH/HEIGHT` (UnsignedInt): Default icon dimensions
- `SICKLY_GREEN_POISONED_COLOR` (RGBColor): Color for poisoned state
- `DARK_GRAY_DISABLED_COLOR` (RGBColor): Color for disabled state
- `RED_IRRADIATED_COLOR` (RGBColor): Color for irradiated state
- `SUBDUAL_DAMAGE_COLOR` (RGBColor): Color for subdual damage
- `FRENZY_COLOR` (RGBColor): Color for frenzy state
- `FRENZY_COLOR_INFANTRY` (RGBColor): Color for infantry frenzy
- `MAX_ENABLED_MODULES` (Int): Maximum enabled modules per drawable
- `FADE_RATE_EPSILON` (Real): Small value for fade rate comparisons

## Dependencies
- Common game systems (Audio, GameEngine, Player)
- GameLogic modules (AIUpdate, BodyModule, etc.)
- GameClient systems (Anim2D, Display, Image)
- Serialization (Xfer)
- Math utilities (Vector3)
