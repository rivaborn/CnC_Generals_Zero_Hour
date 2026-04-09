# Generals/Code/Tools/WW3D/max2w3d/AlphaModifier.h - Enhanced Analysis

## Architectural Role
This file defines a 3DS Max modifier plugin specifically for WW3D (Westwood 3D) model pipeline, enabling alpha channel manipulation during model export. It bridges 3DS Max's modifier system with WW3D's vertex channel requirements.

## Cross-References
### Incoming
- `max2w3d` export tool (calls `Get_Alpha_Desc` for plugin registration)
- 3DS Max modifier stack (calls `ModifyObject` during evaluation)
- Parameter UI system (calls `BeginEditParams`/`EndEditParams`)

### Outgoing
- 3DS Max SDK (`<max.h>`) for modifier infrastructure
- Parameter block system (`<iparamm2.h>`) for UI/serialization
- Mesh manipulation utilities (`<meshadj.h>`) for vertex editing

## Design Patterns
- **Plugin Architecture**: Follows 3DS Max's modifier plugin pattern for extensibility
- **Parameter Block**: Uses `IParamBlock2` for serialized modifier settings
- **Observer Pattern**: `NotifyInputChanged` implements dependency tracking for modifier stack updates

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
