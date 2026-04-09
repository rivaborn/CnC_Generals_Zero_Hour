# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Shell/ShellMenuScheme.cpp

## Purpose
Handles the loading, management, and rendering of shell menu schemes in the game UI.

## Responsibilities
- Parses INI configuration for menu schemes
- Manages a collection of menu schemes
- Renders images and lines for the current scheme
- Provides access to active scheme for drawing

## Key Types
- **ShellMenuSchemeManager (Class)**: Manages collection of menu schemes and current active scheme
- **ShellMenuScheme (Class)**: Represents a menu scheme containing images and lines
- **ShellMenuSchemeImage (Class)**: Stores image data (position, size, image reference)
- **ShellMenuSchemeLine (Class)**: Stores line data (start/end positions, color, width)

## Key Functions
### parseImagePart
- Purpose: Parses image configuration from INI and creates ShellMenuSchemeImage
- Calls: INI::parseICoord2D, INI::parseMappedImage, ShellMenuScheme::addImage

### parseLinePart
- Purpose: Parses line configuration from INI and creates ShellMenuSchemeLine
- Calls: INI::parseICoord2D, INI::parseColorInt, INI::parseInt, ShellMenuScheme::addLine

### newShellMenuScheme
- Purpose: Creates or replaces a menu scheme with given name
- Calls: None

### draw
- Purpose: Renders the current active menu scheme
- Calls: ShellMenuScheme::draw

## Globals
- **m_shellMenuSchemeFieldParseTable (FieldParse[])**: Parsing rules for menu scheme INI sections

## Dependencies
- Common/INI.h (INI parsing)
- GameClient/ShellMenuScheme.h (header)
- GameClient/Shell.h (TheShell access)
- GameClient/Display.h (TheDisplay access)
