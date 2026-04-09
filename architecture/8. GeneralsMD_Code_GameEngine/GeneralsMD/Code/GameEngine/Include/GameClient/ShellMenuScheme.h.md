# GeneralsMD/Code/GameEngine/Include/GameClient/ShellMenuScheme.h

## Purpose
Defines classes for managing shell menu schemes, including images and lines, and parsing them from INI files.

## Responsibilities
- Define data structures for shell menu elements (images, lines)
- Manage a collection of shell menu schemes
- Parse shell menu schemes from INI files
- Provide drawing functionality for shell menus

## Key Types
- **ShellMenuSchemeLine (Class)**: Represents a line in a shell menu with position, width, and color.
- **ShellMenuSchemeImage (Class)**: Represents an image in a shell menu with name, position, size, and image pointer.
- **ShellMenuScheme (Class)**: Manages a collection of images and lines for a shell menu scheme.
- **ShellMenuSchemeManager (Class)**: Manages multiple shell menu schemes, parsing, and rendering.
- **Image (Class)**: Forward reference to an image class (not defined here).

## Key Functions
### ShellMenuScheme::draw
- Purpose: Draws the shell menu scheme.
- Calls: Not inferable.

### ShellMenuSchemeManager::setShellMenuScheme
- Purpose: Sets the current shell menu scheme by name.
- Calls: Not inferable.

### ShellMenuSchemeManager::draw
- Purpose: Draws the current shell menu scheme.
- Calls: Not inferable.

### ShellMenuSchemeManager::parseImagePart
- Purpose: Parses the image part of an INI file.
- Calls: Not inferable.

### ShellMenuSchemeManager::parseLinePart
- Purpose: Parses the line part of an INI file.
- Calls: Not inferable.

## Globals
- **m_shellMenuSchemeFieldParseTable (FieldParse[])**: Static parse table for INI file parsing.

## Dependencies
- Key includes: `GameClient/Color.h`
- External
