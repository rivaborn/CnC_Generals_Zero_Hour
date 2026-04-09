# Generals/Code/GameEngine/Source/GameClient/GUI/GameWindowTransitions.cpp

## Purpose
Manages window transition effects in the game UI, including loading transition definitions from INI files and handling transition groups.

## Responsibilities
- Loads and parses window transition definitions from INI files
- Manages transition groups and their lifecycle (init, update, draw, reverse)
- Provides factory function for creating specific transition types
- Handles transition state (current, pending, draw groups)

## Key Types
- **TransitionGroup (Class)**: Manages a collection of transition windows and their timing
- **TransitionWindow (Class)**: Represents a single window with a transition effect
- **GameWindowTransitionsHandler (Class)**: Main class that coordinates all transitions and groups
- **Transition (Base Class)**: Abstract base for all transition types (not shown in this file)
- **TransitionStyleNames (Lookup List)**: Maps transition style names to enum values

## Key Functions
### getTransitionForStyle
- Purpose: Factory function that creates transition objects based on style enum
- Calls: NEW operator for specific transition types (FlashTransition, ButtonFlashTransition, etc.)

### parseWindowTransitions
- Purpose: Parses window transition definitions from INI files
- Calls: TheTransitionHandler->getNewGroup, ini->initFromINI

### GameWindowTransitionsHandler::update
- Purpose: Updates all active transitions and manages group transitions
- Calls: m_currentGroup->update, m_currentGroup->isFinished, m_currentGroup->isFireOnce

### GameWindowTransitionsHandler::draw
- Purpose: Renders all active transitions
- Calls: m_drawGroup->draw, m_secondaryDrawGroup->draw

## Globals
- **TheTransitionHandler (GameWindowTransitionsHandler*)**: Global instance of the transition handler
- **m_gameWindowTransitionsFieldParseTable (FieldParse[])**: INI parsing table for transition groups

## Dependencies
- GameWindowTransitions.h (header for this file)
- GameWindow.h, GameWindowManager.h (window system)
- GameLogic.h (game state)
- INI parsing system (INI class)
- NameKeyGenerator (for window name lookup)
- Various transition subclasses (FlashTransition, FadeTransition, etc.)
