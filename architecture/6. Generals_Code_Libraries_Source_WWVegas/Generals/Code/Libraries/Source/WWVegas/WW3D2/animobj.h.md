# Generals/Code/Libraries/Source/WWVegas/WW3D2/animobj.h

## Purpose
Defines the `Animatable3DObjClass` for hierarchical animation in the SAGE engine, managing bone transforms and animation states.

## Responsibilities
- Manages hierarchical animation via `HTreeClass`
- Handles bone transforms and animation blending
- Provides rendering and scene graph integration
- Supports multiple animation modes (single, blend, combo)
- Tracks animation state and frame progression

## Key Types
- **Animatable3DObjClass (Class)**: Core class for hierarchical animation.
- **HTreeClass (Class)**: Hierarchy tree for bone transforms (external).
- **HAnimClass (Class)**: Base animation class (external).
- **HAnimComboClass (Class)**: Animation combination class (external).
- **CurMotionMode (Enum)**: Animation state (NONE, BASE_POSE, SINGLE_ANIM, DOUBLE_ANIM, MULTIPLE_ANIM).

## Key Functions
### `Set_Animation`
- Purpose: Configures animation state (single, blend, or combo).
- Calls: `Release()`, `Set_Hierarchy_Valid()`.

### `Update_Sub_Object_Transforms`
- Purpose: Updates transforms based on current animation state.
- Calls: `Base_Update()`, `Anim_Update()`, `Blend_Update()`, `Combo_Update()`.

### `Base_Update`
- Purpose: Applies base pose to hierarchy.
- Calls: `HTree->Base_Update()`.

### `Anim_Update`
- Purpose: Applies single animation to hierarchy.
- Calls: `HTree->Anim_Update()`.

### `Blend_Update`
- Purpose: Blends two animations.
- Calls: `HTree->Blend_Update()`.

### `Combo_Update`
- Purpose: Applies animation combination.
- Calls: `HTree->Combo_Update()`.

## Globals
- **IsTreeValid (bool)**: Tracks hierarchy validity (mutable).
- **HTree (HTreeClass*)**: Pointer to hierarchy tree.

## Dependencies
- `composite.h` (CompositeRenderObjClass)
- `htree.h` (HTreeClass)
- `hanim.h` (HAnimClass, HAnimComboClass)
- `always.h` (likely for macros/constants)
