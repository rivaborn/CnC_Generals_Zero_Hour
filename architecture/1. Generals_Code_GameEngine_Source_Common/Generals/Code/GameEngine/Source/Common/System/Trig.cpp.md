# Generals/Code/GameEngine/Source/Common/System/Trig.cpp

The provided code defines a custom trigonometric library using integer arithmetic for fixed-point calculations. It includes functions like `Sin`, `Cos`, `Tan`, `ACos`, and `ASin`. The library uses lookup tables to store precomputed sine values and arc cosine values, which allows for faster computation compared to standard floating-point trigonometric functions.

Key features:
- **Fixed-Point Arithmetic**: Uses integer constants (`INT_ONE`, `INT_TWOPI`) to represent real numbers.
- **Lookup Tables**: Precomputes sine values in `sinLookup` and arc cosine values in `arcCosLookup`.
- **Angle Normalization**: Ensures angles are within the range [0, 2Ï) for sine and tangent calculations.
- **Regeneration Script**: Includes a script to regenerate the lookup tables if needed.

This approach is useful for systems where floating-point operations are expensive or unavailable.
