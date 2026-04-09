# GeneralsMD/Code/GameEngine/Include/Common/Player.h - Enhanced Analysis

## Architectural Role
Central class representing a game participant, bridging game logic (AI, economy), rendering (color management), and networking (player relations). Acts as the primary container for player state, resources, and capabilities.

## Cross-References
### Incoming
- AIPlayer.h (inherits Player, implements AI-specific behavior)
- AISkirmishPlayer.h (specialized AI behavior)
- LANPlayer.h (networking-specific player data)
- GameLogic modules (build logic, upgrade handling)

### Outgoing
- Common subsystems (Energy, Money, Science, Upgrade)
- GameLogic (AIPlayer, Team)
- Networking (PlayerRelationMap, TeamRelationMap)
- UI (ScoreKeeper, AcademyStats)

## Design Patterns
- **Composite**: Player contains multiple Team instances via m_playerTeamPrototypes
- **Observer**: SpecialPowerReadyTimerList tracks cooldown events
- **Strategy**: BattlePlanBonuses encapsulates different battle plan behaviors

*Not inferable*: Exact implementation of production cost/time modifiers (m_productionCostChanges/m_productionTimeChanges)
