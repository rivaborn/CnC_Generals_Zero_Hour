# Generals/Code/Tools/WorldBuilder/src/SplashScreen.cpp

## Purpose
Handles the splash screen UI in the WorldBuilder tool, displaying loading text.

## Responsibilities
- Manages splash screen rectangle and font
- Loads and displays localized strings
- Handles paint events for text rendering

## Key Types
- SplashScreen (class): splash screen UI control
- LOGFONT (struct): font configuration

## Key Functions
### SplashScreen::SplashScreen()
- Purpose: Constructor initializes splash screen state
- Calls: None

### SplashScreen::setTextOutputLocation()
- Purpose: Sets the rectangle where text will be drawn
- Calls: None

### SplashScreen::outputText()
- Purpose: Loads and displays a string resource
- Calls: CString::LoadString(), RedrawWindow()

### SplashScreen::OnPaint()
- Purpose: Handles paint event to render splash text
- Calls: CDialog::OnPaint(), GetDC(), CFont::SelectObject(), CDC::SetTextColor()

## Globals
- None

## Dependencies
- StdAfx.h, SplashScreen.h
- MFC classes: CDialog, CString, CRect, CDC, CFont
- Windows API: LOGFONT, COLORREF, RedrawWindow()
