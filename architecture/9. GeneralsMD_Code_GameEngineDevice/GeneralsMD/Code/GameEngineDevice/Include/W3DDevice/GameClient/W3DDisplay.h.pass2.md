# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDisplay.h - Enhanced Analysis

## Architectural Role
This header defines the core rendering interface for the SAGE engine's W3D backend, bridging high-level display management with low-level 3D/2D rendering. It serves as the primary abstraction for all visual output, coordinating between scene management, asset handling, and performance monitoring.

## Cross-References
### Incoming
- Game logic systems (e.g., UI, HUD) call drawing primitives (drawLine, drawImage)
- Mission/terrain systems use setShroudLevel and clearShroud
- Debug systems access FPS stats and debug display strings
- Network code references NetStats display strings

### Outgoing
- Directly interfaces with WW3D2's LightEnvironmentClass for lighting
- Uses Render2DClass for 2D operations
- Manages RTS3DScene/RTS2DScene for scene composition
- Depends on W3DAssetManager for resource handling

## Design Patterns
- **Singleton-like static members** (m_3DScene, m_assetManager) for global resource access, though not strictly singletons
- **Facade pattern** - W3DDisplay abstracts complex W3D rendering into simpler interfaces
- **Observer pattern** implied by debug display strings (DisplayString array) for performance metrics

*Not inferable: Exact implementation of LightClass management or scene rendering pipeline.*
