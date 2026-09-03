### Ticket Number: 001
### Title: External Keyboard Executing Commands Instead of Typing
### Date: 2026-09-03
### Category: Hardware / Peripherals

**Reported Issue:**
User plugged external keyboard into laptop. When typing, it executed shortcut commands (e.g., P for Print).

**Root Cause:**
Stuck Ctrl/Alt modifier key on laptop keyboard interfering with external keyboard input. Sticky Keys possibly triggered.

**Troubleshooting Steps:**
1. Pressed and released both Ctrl, Alt, Shift keys 5x, Esc 3x, Windows key 2x
2. Checked laptop keyboard for physically stuck keys
3. Tested typing in Notepad to isolate app vs system
4. Verified Sticky Keys, Filter Keys OFF in Accessibility settings
5. Unplugged and replugged keyboard to different USB port

**Solution:**
Released stuck modifier keys by tapping Ctrl+Alt+Esc. Keyboard resumed normal typing.

**Time to Resolve:** 2 minutes
**Prevention:** Avoid placing objects on laptop keyboard, clean keys regularly, disable Sticky Keys.
