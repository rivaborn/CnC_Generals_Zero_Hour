# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDisplayStringManager.h

## Purpose
Manages game display strings for the W3D rendering system, providing allocation, updates, and shared numeral/formation strings.

## Responsibilities
- Manages creation and lifecycle of display strings
- Provides shared numeral and formation letter strings
- Updates all managed display strings
- Initializes numeral strings post-load

## Key Types
- W3DDisplayStringManager (Class): Manages display strings for W3D rendering

## Key Functions
### W3DDisplayStringManager()
- Purpose: Constructor for display string manager
- Calls: Not inferable

### ~W3DDisplayStringManager()
- Purpose: Destructor for display string manager
- Calls: Not inferable

### postProcessLoad()
- Purpose: Initializes numeral strings after loading
- Calls: Not inferable

### update()
- Purpose: Updates all managed display strings
- Calls: Not inferable

### newDisplayString()
- Purpose: Allocates a new display string
- Calls: Not inferable

### freeDisplayString()
- Purpose: Frees a display string
- Calls: Not inferable

### getGroupNumeralString()
- Purpose: Returns shared numeral string for groups
- Calls: Not inferable

### getFormationLetterString()
- Purpose: Returns shared formation letter string
- Calls: Not inferable

## Globals
- MAX_GROUPS (const int): Maximum number of group numeral strings (10 or 20)

## Dependencies
- DisplayStringManager (base class)
- W3DDisplayString (included header)
- DisplayString (used in method signatures)
