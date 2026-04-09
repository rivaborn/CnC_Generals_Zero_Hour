# Generals/Code/Libraries/Source/WWVegas/WWLib/mpu.cpp

## Purpose
Provides CPU performance measurement utilities using Windows high-resolution timers and the RDTSC instruction.

## Responsibilities
- Measures CPU clock rate using QueryPerformanceCounter
- Determines CPU speed via Time Stamp Counter (RDTSC)
- Handles priority adjustments for accurate timing
- Performs multiple samples to improve measurement accuracy

## Key Types
- QuadValue (Union): Wraps LARGE_INTEGER with QuadPart accessors
- QuadPart (Struct): Contains LowPart/HighPart for 64-bit value access

## Key Functions
### Get_CPU_Rate
- Purpose: Retrieves CPU ticks per second via QueryPerformanceFrequency
- Calls: QueryPerformanceFrequency

### Get_CPU_Clock
- Purpose: Reads CPU time stamp counter via inline assembly
- Calls: None (uses inline asm)

### RDTSC
- Purpose: Reads Time Stamp Counter into global variables
- Calls: None (uses inline asm)

### Get_RDTSC_CPU_Speed
- Purpose: Calculates CPU speed in MHz using multiple RDTSC samples
- Calls: QueryPerformanceCounter, QueryPerformanceFrequency, GetPriorityClass, SetPriorityClass, GetThreadPriority, SetThreadPriority

## Globals
- TSC_Low (unsigned long): Stores low 32 bits of RDTSC result
- TSC_High (unsigned long): Stores high 32 bits of RDTSC result

## Dependencies
- always.h, win.h, mpu.h, math.h, assert.h
- Windows API: QueryPerformanceCounter/Frequency, Get/SetPriorityClass/ThreadPriority
- Inline assembly for RDTSC instruction
