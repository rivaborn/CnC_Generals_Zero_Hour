# Generals/Code/Tools/ParticleEditor/VelocityTypePanels.h

## Purpose
Defines UI panels for editing different particle velocity types in the Particle Editor tool.

## Responsibilities
- Provide specialized panels for Ortho, Sphere, Hemisphere, Cylinder, and Outward velocity types
- Handle UI initialization and updates between UI and particle system
- Manage message handling for particle system edits

## Key Types
- VelocityPanelOrtho (Class): Panel for orthogonal velocity editing
- VelocityPanelSphere (Class): Panel for spherical velocity editing
- VelocityPanelHemisphere (Class): Panel for hemispherical velocity editing
- VelocityPanelCylinder (Class): Panel for cylindrical velocity editing
- VelocityPanelOutward (Class): Panel for outward velocity editing
- IDD (Enum): Dialog resource IDs for each panel type

## Key Functions
### VelocityPanelOrtho/InitPanel
- Purpose: Initialize the Ortho velocity panel UI
- Calls: Not inferable

### VelocityPanelOrtho/performUpdate
- Purpose: Synchronize between UI and particle system
- Calls: Not inferable

### VelocityPanelOrtho/OnParticleSystemEdit
- Purpose: Handle particle system edit events
- Calls: Not inferable

## Globals
- None

## Dependencies
- ISwapablePanel: Base class for panel interface
- resource.h: For dialog resource IDs
- MFC classes (CWnd, afx_msg, DECLARE_MESSAGE_MAP)
