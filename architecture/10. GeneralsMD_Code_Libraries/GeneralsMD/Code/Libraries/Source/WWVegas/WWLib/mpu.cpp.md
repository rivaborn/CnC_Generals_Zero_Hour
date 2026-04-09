# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mpu.cpp

## Purpose
This file provides CPU performance measurement utilities, including clock rate and frequency detection.

## Responsibilities
- Fetch CPU clock rate using high-resolution performance counters
- Measure CPU frequency via Time Stamp Counter (TSC)
- Provide low-level CPU timing primitives

## Key Types
- QuadValue (Union): Wraps LARGE_INTEGER with QuadPart accessors
- QuadPart (Struct): Contains LowPart and HighPart unsigned longs

## Key Functions
### Get_CPU_Rate
- Purpose: Retrieves CPU ticks per second via QueryPerformanceFrequency
- Calls: QueryPerformanceFrequency

### Get_CPU_Clock
- Purpose: Reads CPU time stamp counter directly via inline assembly
- Calls: None (uses inline asm)

### RDTSC
- Purpose: Reads Time Stamp Counter into global variables
- Calls: None (uses inline asm)

### Get_RDTSC_CPU_Speed
- Purpose: Calculates CPU speed in MHz by comparing TSC with performance counter
- Calls: QueryPerformanceFrequency, QueryPerformanceCounter, GetPriorityClass, SetPriorityClass, GetThreadPriority, SetThreadPriority

## Globals
- TSC_Low (unsigned long): Stores low 32 bits of TSC
- TSC_High (unsigned long): Stores high 32 bits of TSC

## Dependencies
- always.h, win.h, mpu.h, math.h, assert.h
- QueryPerformanceFrequency, QueryPerformanceCounter, GetPriorityClass, SetPriorityClass, GetThreadPriority, SetThreadPriority
