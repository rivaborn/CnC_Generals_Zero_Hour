# GeneralsMD/Code/GameEngine/Source/Common/INI/INIParticleSys.cpp

## Purpose
Parses particle system definitions from INI files into runtime templates.

## Responsibilities
- Reads particle system name from INI token
- Locates or creates a ParticleSystemTemplate
- Delegates INI parsing to the template's field parser

## Key Types
- None

## Key Functions
### parseParticleSystemDefinition
- Purpose: Parses a particle system definition from an INI file
- Calls: `ini->getNextToken()`, `TheParticleSystemManager->findTemplate()`, `TheParticleSystemManager->newTemplate()`, `ini->initFromINI()`

## Globals
- None

## Dependencies
- `INI.h` (INI class)
- `GameClient/ParticleSys.h` (ParticleSystemTemplate, TheParticleSystemManager)
- `PreRTS.h` (header inclusion guard)
