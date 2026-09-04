### Ticket Number: 002
### Title: Display Zoomed In - Magnifier Stuck On Login Screen
### Date: 2026-09-04
### Category: OS

**Reported Issue:**
User reported screen was expanded/enlarged on login screen, could not see full display, only part of options visible.

**Root Cause:**
Windows Magnifier was accidentally triggered and left at 200%+ zoom.

**Troubleshooting Steps:**
1. Observed display was magnified, not resolution issue
2. Pressed Windows Key + Minus (-) to zoom out
3. Pressed Windows Key + Esc to fully exit Magnifier

**Solution:**
Fixed by zooming out with Windows + - and closing Magnifier with Windows + Esc. Display restored to normal 100%.

**Time to Resolve:** < 1 min
**Prevention:** Informed user about Magnifier shortcut (Windows + Plus / Minus) to avoid accidental activation.
