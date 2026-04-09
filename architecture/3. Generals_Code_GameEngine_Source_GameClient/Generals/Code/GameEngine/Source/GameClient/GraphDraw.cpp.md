# Generals/Code/GameEngine/Source/GameClient/GraphDraw.cpp

## Purpose
Handles queuing and rendering performance graphs for debugging, enabled only when PERF_TIMERS is defined.

## Responsibilities
- Manages graph entries (labels and values)
- Renders performance bars on screen
- Creates/frees display strings for text rendering
- Clears graph data when needed

## Key Types
- GraphDraw (Class): Main graph rendering class
- MAX_GRAPH_VALUES (const): Maximum number of graph entries (10)
- BAR_HEIGHT (const): Height of each bar (16)
- BAR_SPACE (const): Space between bars (2)

## Key Functions
### GraphDraw::GraphDraw()
- Purpose: Constructor initializes display strings for graph labels
- Calls: TheFontLibrary->getFont(), TheDisplayStringManager->newDisplayString()

### GraphDraw::render()
- Purpose: Renders all graph entries as horizontal bars with labels
- Calls: TheDisplay->getWidth(), TheDisplay->getHeight(), TheDisplay->drawFillRect(), m_displayStrings[count]->draw()

### GraphDraw::addEntry()
- Purpose: Adds a new entry (label and value) to the graph
- Calls: m_graphEntries.push_back()

### GraphDraw::clear()
- Purpose: Clears all graph entries
- Calls: m_graphEntries.clear()

## Globals
- TheGraphDraw (GraphDraw*): Singleton instance of GraphDraw (only if PERF_TIMERS defined)

## Dependencies
- PreRTS.h, GraphDraw.h, Display.h, DisplayString.h, DisplayStringManager.h
- TheDisplay, TheFontLibrary, TheDisplayStringManager singletons
- std::pair, std::vector, UnicodeString, VecGraphEntriesIt (iterator)
