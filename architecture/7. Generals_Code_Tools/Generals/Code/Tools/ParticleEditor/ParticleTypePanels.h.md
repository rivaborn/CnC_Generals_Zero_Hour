# Generals/Code/Tools/ParticleEditor/ParticleTypePanels.h

## Purpose
Defines UI panels for editing particle system properties in the Particle Editor tool.

## Responsibilities
- Provide dialog classes for particle, drawable, and streak properties
- Manage UI updates between the editor and particle system
- Handle initialization and cleanup of panel controls

## Key Types
- **ParticlePanelParticle (Class)**: Base panel for particle properties.
- **ParticlePanelDrawable (Class)**: Panel for drawable particle properties.
- **ParticlePanelStreak (Class)**: Panel for streak particle properties (inherits from ParticlePanelParticle).
- **IDD (Enum)**: Dialog resource IDs for each panel type.

## Key Functions
### ParticlePanelParticle/performUpdate
- Purpose: Synchronizes UI and particle system data.
- Calls: Not inferable.

### ParticlePanelDrawable/clearAllThingTemplates
- Purpose: Clears all thing templates from the drawable panel.
- Calls: Not inferable.

### ParticlePanelStreak/performUpdate
- Purpose: Synchronizes UI and streak particle system data.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `resource.h`: Dialog resource definitions.
- `ISwapablePanel`: Base class for swapable panels.
