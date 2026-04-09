# GeneralsMD/Code/GameEngine/Source/Common/INI/INIMappedImage.cpp

## Purpose
Parses mapped image definitions from INI files into Image objects.

## Responsibilities
- Reads INI tokens to extract image names
- Creates or updates Image objects in TheMappedImageCollection
- Validates existing images before parsing
- Delegates field parsing to Image's own parser

## Key Types
- None (only functions and globals)

## Key Functions
### parseMappedImageDefinition
- Purpose: Parses a mapped image entry from an INI file.
- Calls:
  - ini->getNextToken()
  - TheMappedImageCollection->findImageByName()
  - newInstance(Image)
  - image->setName()
  - TheMappedImageCollection->addImage()
  - ini->initFromINI()
  - image->getFieldParse()

## Globals
- TheMappedImageCollection (MappedImageCollection*): Holds all parsed Image objects.

## Dependencies
- "Common/INI.h" (INI class)
- "GameClient/Image.h" (Image class)
- newInstance template function
- DEBUG_ASSERTCRASH macro
