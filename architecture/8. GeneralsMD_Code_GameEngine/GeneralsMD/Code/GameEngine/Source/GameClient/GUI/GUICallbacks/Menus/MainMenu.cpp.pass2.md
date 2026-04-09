# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/MainMenu.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central hub for main menu functionality, bridging UI input handling with game initialization systems. It coordinates between the window management system, campaign management, and transition effects to create a cohesive menu experience.

## Cross-References
### Incoming
- `GameClient/Shell.cpp` (pushes menu states)
- `GameClient/GameWindowManager.cpp` (window layout creation/destruction)
- `GameClient/CampaignManager.cpp` (campaign selection)
- `GameNetwork/GameSpyOverlay.cpp` (online menu integration)

### Outgoing
- `GameClient/WindowLayout` (menu UI construction)
- `GameClient/GameWindowTransitions` (menu animations)
- `GameClient/CDCheck` (copy protection)
- `GameLogic/GameLogic` (game initialization)

## Design Patterns
- **Command Pattern**: Menu actions are encapsulated as callbacks, decoupling UI events from game logic
- **State Pattern**: Menu navigation implicitly manages state transitions through window visibility and transition groups
- **Singleton Access**: Heavy use of global managers (TheCampaignManager, TheTransitionHandler) for system coordination

Rules followed. Output under 400 tokens.
