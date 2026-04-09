# Generals/Code/Tools/timingTest/StdAfx.h

## Purpose
Precompiled header file for the timingTest tool, including standard system headers and project-specific common includes.

## Responsibilities
- Defines include guards for the header
- Includes Windows lean-and-mean headers
- Provides standard C library headers
- Marks location for additional project-specific includes

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- `<stdio.h>` (C standard I/O)
- Windows SDK headers (via `WIN32_LEAN_AND_MEAN`)
- Microsoft-specific precompiled header markers (`AFX_INSERT_LOCATION`)
