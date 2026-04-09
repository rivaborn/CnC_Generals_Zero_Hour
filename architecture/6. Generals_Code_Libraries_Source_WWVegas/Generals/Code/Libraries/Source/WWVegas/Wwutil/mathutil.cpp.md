# Generals/Code/Libraries/Source/WWVegas/Wwutil/mathutil.cpp

## Purpose
Provides utility functions for mathematical operations, including vector/angle conversions, distance calculations, and random number generation.

## Responsibilities
- Convert between angles and vectors
- Calculate distances between points
- Round floating-point values
- Rotate vectors
- Generate random numbers with different distributions

## Key Types
- cMathUtil (Class): namespace for math utilities

## Key Functions
### Angle_To_Vector
- Purpose: Converts an angle to a unit vector
- Calls: WWMath::Sin, WWMath::Cos, ::sqrt, WWASSERT

### Vector_To_Angle
- Purpose: Converts a vector to an angle
- Calls: WWMath::Atan, WWASSERT

### Simple_Distance
- Purpose: Calculates Euclidean distance between two points
- Calls: ::sqrt

### Round
- Purpose: Rounds a double to nearest integer
- Calls: None

### Rotate_Vector
- Purpose: Rotates a vector by a given angle
- Calls: WWMath::Cos, WWMath::Sin

### Get_Uniform_Pdf_Double
- Purpose: Generates a random double in a range with uniform distribution
- Calls: ::rand, WWASSERT

### Get_Normalized_Uniform_Pdf_Double
- Purpose: Generates a random double between 0 and 1
- Calls: Get_Uniform_Pdf_Double

### Get_Uniform_Pdf_Int
- Purpose: Generates a random integer in a range
- Calls: ::rand, WWASSERT

### Get_Hat_Pdf_Double
- Purpose: Generates a random double with triangular distribution
- Calls: Get_Uniform_Pdf_Double, WWASSERT

### Get_Normalized_Hat_Pdf_Double
- Purpose: Generates a random double between 0 and 1 with triangular distribution
- Calls: Get_Hat_Pdf_Double

### Get_Hat_Pdf_Int
- Purpose: Generates a random integer with triangular distribution
- Calls: Round, Get_Hat_Pdf_Double

## Globals
- PI (double): Value of Ï
- PI_2 (double): Value of Ï/2

## Dependencies
- mathutil.h, math.h, stdlib.h, wwmath.h, miscutil.h, wwdebug.h
- WWMath, WWASSERT, MISCUTIL_EPSILON, WWMATH_EPSILON
