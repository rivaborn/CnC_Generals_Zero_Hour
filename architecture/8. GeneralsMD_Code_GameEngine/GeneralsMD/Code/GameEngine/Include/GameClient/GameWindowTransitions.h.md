# GeneralsMD/Code/GameEngine/Include/GameClient/GameWindowTransitions.h

## Purpose
Header file defining UI transition effects for the game client, including fade, scale, and text animations.

## Responsibilities
- Declares transition classes for UI animations
- Defines transition types and their states
- Provides transition management system via GameWindowTransitionsHandler
- Includes parsing infrastructure for INI configuration

## Key Types
- Transition (Class): base class for all UI transitions
- TextOnFrameTransition (Class): text display transition
- ReverseSoundTransition (Class): sound-based transition
- FullFadeTransition (Class): full-screen fade effect
- ControlBarArrowTransition (Class): control bar arrow animation
- ScreenFadeTransition (Class): screen fade effect
- CountUpTransition (Class): counting animation
- TextTypeTransition (Class): text typing animation
- MainMenuScaleUpTransition (Class): main menu scale effect
- MainMenuMediumScaleUpTransition (Class): medium scale effect
- MainMenuSmallScaleDownTransition (Class): small scale down effect
- ScaleUpTransition (Class): general scale up effect
- ScoreScaleUpTransition (Class): score display animation
- FadeTransition (Class): fade animation
- FlashTransition (Class): flash effect
- ButtonFlashTransition (Class): button flash effect
- TransitionWindow (Class): container for individual window transitions
- TransitionGroup (Class): groups multiple transitions
- GameWindowTransitionsHandler (Class): manages all transitions
- (anonymous enum): defines transition style constants

## Key Functions
### PushButtonImageDrawThree
- Purpose: Draws a button image with three states
- Calls: Not inferable

## Globals
- TransitionStyleNames (LookupListRec[]): maps transition style names to enum values
- TheTransitionHandler (GameWindowTransitionsHandler*): global transition handler instance

## Dependencies
- GameWindow, Image, DisplayString (forward declarations)
- SubsystemInterface (inheritance)
- INI, FieldParse (parsing infrastructure)
- std::list (container)
- ICoord2D, Real, Bool, Int, UnicodeString, AsciiString, NameKeyType (types)
