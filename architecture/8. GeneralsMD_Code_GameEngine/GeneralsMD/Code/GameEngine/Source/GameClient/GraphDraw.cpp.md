# GeneralsMD/Code/GameEngine/Source/GameClient/GraphDraw.cpp

## Purpose
Handles queuing and rendering performance graphs for debugging purposes.

## Responsibilities
- Manages graph entries (labels and values)
- Renders graph bars and labels on screen
- Clears graph data when needed

## Key Types
- `GraphDraw` (Class): Main graph rendering class
- `MAX_GRAPH_VALUES` (const): Maximum number of graph entries
- `BAR_HEIGHT` (const): Height of each graph bar
- `BAR_SPACE` (const): Space between bars

## Key Functions
### `GraphDraw::GraphDraw()`
- Purpose: Constructor initializes display strings for graph labels
- Calls: `TheDisplayStringManager->newDisplayString()`, `TheFontLibrary->getFont()`

### `GraphDraw::~GraphDraw()`
- Purpose: Destructor cleans up display strings
- Calls: `TheDisplayStringManager->freeDisplayString()`

### `GraphDraw::addEntry()`
- Purpose: Adds a new graph entry with label and value
- Calls: `m_graphEntries.push_back()`

### `GraphDraw::render()`
- Purpose: Renders all graph entries as horizontal bars
- Calls: `TheDisplay->getWidth()`, `TheDisplay->getHeight()`, `TheDisplay->drawFillRect()`, `m_displayStrings[count]->draw()`

### `GraphDraw::clear()`
- Purpose: Clears all graph entries
- Calls: `m_graphEntries.clear()`

## Globals
- `TheGraphDraw` (GraphDraw*): Singleton instance of GraphDraw

## Dependencies
- `PreRTS.h`, `GraphDraw.h`, `Display.h`, `DisplayString.h`, `DisplayStringManager.h`
- `TheDisplay`, `TheDisplayStringManager`, `TheFontLibrary` (external singletons)
- `AsciiString
