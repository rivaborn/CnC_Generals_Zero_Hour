# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindowTransitions.cpp

## Purpose
Manages window transition effects in the game UI, including loading transition definitions from INI files and handling transition groups.

## Responsibilities
- Loads and parses window transition definitions from INI files
- Manages transition groups and their states (playing, reversed, finished)
- Provides factory function for creating specific transition types
- Handles transition updates and rendering

## Key Types
- **TransitionGroup (Class)**: Manages a collection of transition windows and their playback state
- **TransitionWindow (Class)**: Represents a single window with a transition effect
- **GameWindowTransitionsHandler (Class)**: Main handler for managing all transitions and groups
- **TransitionStyleNames (Not inferable)**: Enum or array defining transition style types

## Key Functions
### getTransitionForStyle
- Purpose: Factory function that creates transition objects based on style enum
- Calls: NEW operator for various transition classes (FlashTransition, ButtonFlashTransition, etc.)

### parseWindowTransitions
- Purpose: Parses window transition definitions from INI files
- Calls: TheTransitionHandler->getNewGroup, ini->initFromINI

### GameWindowTransitionsHandler::update
- Purpose: Updates all active transitions and manages state transitions
- Calls: m_currentGroup->update, m_currentGroup->isFinished, m_currentGroup->isFireOnce

### GameWindowTransitionsHandler::draw
- Purpose: Renders all active transitions
- Calls: m_drawGroup->draw, m_secondaryDrawGroup->draw

## Globals
- **TheTransitionHandler (GameWindowTransitionsHandler*)**: Global instance of the transition handler
- **m_gameWindowTransitionsFieldParseTable (FieldParse[])**: Field parse table for INI parsing

## Dependencies
- GameWindowTransitions.h, GameWindow.h, GameWindowManager.h
- INI class for configuration parsing
- Various transition classes (FlashTransition, FadeTransition, etc.)
- NameKeyGenerator for window name resolution
