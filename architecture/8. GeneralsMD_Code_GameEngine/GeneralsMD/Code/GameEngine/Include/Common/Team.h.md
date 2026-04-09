# GeneralsMD/Code/GameEngine/Include/Common/Team.h

## Purpose
Defines the team system for the game, including team prototypes, instances, and relationships.

## Responsibilities
- Manages team creation, relationships, and state
- Handles team member iteration and counting
- Provides team prototype management and instantiation
- Supports team-specific scripting and behavior

## Key Types
- TeamID (Type): Unique identifier for a team instance
- TeamPrototypeID (Type): Unique identifier for a team prototype
- TeamRelationMap (Class): Stores relationships between teams
- Team (Class): Represents a team instance with members and state
- TeamPrototype (Class): Template for creating team instances
- TeamFactory (Class): Manages team prototypes and instances
- TeamTemplateInfo (Class): Contains team configuration data

## Key Functions
### Team::getRelationship
- Purpose: Returns the relationship between this team and another
- Calls: Accesses m_teamRelations and m_playerRelations

### TeamFactory::createTeam
- Purpose: Creates a new team instance from a prototype
- Calls: Uses m_prototypes map to find prototype

### TeamPrototype::evaluateProductionCondition
- Purpose: Evaluates whether this team should be produced
- Calls: Executes m_productionConditionScript

## Globals
- TheTeamFactory (TeamFactory*): Global instance of the team factory

## Dependencies
- Common/GameType.h
- Common/Snapshot.h
- Common/Thing.h
- GameLogic/Object.h
- std::hash_map, std::list, std::map
- MemoryPoolObject, Snapshot base classes
