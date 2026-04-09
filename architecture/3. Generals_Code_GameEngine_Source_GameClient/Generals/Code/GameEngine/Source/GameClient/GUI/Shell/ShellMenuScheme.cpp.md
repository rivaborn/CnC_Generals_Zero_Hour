# Generals/Code/GameEngine/Source/GameClient/GUI/Shell/ShellMenuScheme.cpp

## Purpose
Manages shell menu schemes, including parsing INI configurations and rendering menu elements.

## Responsibilities
- Parses INI files to load menu schemes
- Manages shell menu scheme objects and their components
- Renders menu images and lines
- Provides scheme switching functionality

## Key Types
- **ShellMenuSchemeManager (Class)**: Manages shell menu schemes and their parsing/rendering
- **ShellMenuScheme (Class)**: Represents a menu scheme containing images and lines
- **ShellMenuSchemeImage (Class)**: Represents an image component in a menu scheme
- **ShellMenuSchemeLine (Class)**: Represents a line component in a menu scheme

## Key Functions
### parseImagePart
- Purpose: Parses image component data from INI
- Calls: INI::parseICoord2D, INI::parseMappedImage, INI::initFromINI

### parseLinePart
- Purpose: Parses line component data from INI
- Calls: INI::parseICoord2D, INI::parseColorInt, INI::parseInt, INI::initFromINI

### draw
- Purpose: Renders all images and lines in the current scheme
- Calls: TheDisplay->drawImage, TheDisplay->drawLine

### newShellMenuScheme
- Purpose: Creates or replaces a shell menu scheme
- Calls: None

## Globals
- **m_shellMenuSchemeFieldParseTable (FieldParse[])**: Field parsing table for shell menu schemes

## Dependencies
- Common/INI.h
- GameClient/ShellMenuScheme.h
- GameClient/Shell.h
- GameClient/Display.h
