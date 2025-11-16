# SnapSide Version 1.0.1 Planning Document

**Status:** Planning Phase  
**Target Release:** TBD (after 1.0 approval)  
**Focus:** Small fixes, improvements, and quality of life enhancements

---

## Overview

Version 1.0.1 will focus on incremental improvements based on initial user feedback and polishing the user experience. This release aims to address minor issues and add small features that enhance usability without major architectural changes.

---

## Planned Features & Improvements

**Scope Summary:**

**1.0.1-core** (Must ship in 1.0.1):
- Custom keyboard shortcuts
- Screenshot preview before copy
- Performance optimizations
- Bug fixes from "Bug Fixes & Known Issues" section

**later (1.1+)** (Stretch goals / future releases):
- Button position memory
- Dark mode visual tweaks
- Window title display
- Multiple button styles
- Sound effects toggle
- Capture counter

### High Priority

#### 1. Custom Keyboard Shortcuts
- **Description:** Allow users to customize the keyboard shortcut beyond ⌘⇧6
- **Rationale:** Different users have different workflow preferences and key conflicts
- **Implementation:** Add settings panel for shortcut customization
- **Estimated Effort:** Medium
- **Priority:** High
- **Scope:** 1.0.1-core

#### 2. Screenshot Preview Before Copy
- **Description:** Show a brief preview of the captured screenshot before auto-copying
- **Rationale:** Users want confirmation of what was captured
- **Implementation:** Display small preview window for 1-2 seconds with option to cancel
- **Estimated Effort:** Medium
- **Priority:** High
- **Scope:** 1.0.1-core

#### 3. Button Position Memory
- **Description:** Remember the last position of the floating button across app restarts
- **Rationale:** Users position the button in convenient locations for their workflow
- **Implementation:** Store button coordinates in UserDefaults
- **Estimated Effort:** Low
- **Priority:** High
- **Scope:** later (1.1+)

### Medium Priority

#### 4. Dark Mode Improvements
- **Description:** Enhance button visibility and appearance in dark mode
- **Rationale:** Current button may not be optimally visible in dark environments
- **Implementation:** Adjust button colors/opacity for better dark mode contrast
- **Estimated Effort:** Low
- **Priority:** Medium
- **Scope:** later (1.1+)

#### 5. Performance Optimizations
- **Description:** Reduce memory footprint and improve screenshot capture speed
- **Rationale:** Better performance = better user experience
- **Implementation:** Profile and optimize image processing pipeline
- **Estimated Effort:** Medium
- **Priority:** Medium
- **Scope:** 1.0.1-core

#### 6. Window Title Display
- **Description:** Briefly show the captured window's title when screenshot is taken
- **Rationale:** Users want confirmation of which window was captured
- **Implementation:** Show temporary overlay with window title
- **Estimated Effort:** Low
- **Priority:** Medium
- **Scope:** later (1.1+)

### Low Priority / Nice to Have

#### 7. Multiple Button Styles
- **Description:** Offer 2-3 different button designs (minimal, classic, modern)
- **Rationale:** Personal preference and aesthetic customization
- **Implementation:** Add button style selector in settings
- **Estimated Effort:** Low
- **Priority:** Low
- **Scope:** later (1.1+)

#### 8. Sound Effects Toggle
- **Description:** Optional audio feedback when screenshot is captured
- **Rationale:** Some users prefer audio confirmation
- **Implementation:** Add toggle in settings + system sound on capture
- **Estimated Effort:** Low
- **Priority:** Low
- **Scope:** later (1.1+)

#### 9. Capture Counter
- **Description:** Show count of screenshots taken in current session
- **Rationale:** Users may want to track their usage
- **Implementation:** Simple counter displayed in menu bar or settings
- **Estimated Effort:** Low
- **Priority:** Low
- **Scope:** later (1.1+)

---

## Bug Fixes & Known Issues

### To Address

1. **Issue:** Button occasionally disappears on external display disconnect
   - **Priority:** High
   - **Status:** Investigating

2. **Issue:** First screenshot after app launch can be slower than subsequent ones
   - **Priority:** Medium
   - **Status:** Known, needs optimization

3. **Issue:** Settings window not accessible if button is hidden
   - **Priority:** Medium  
   - **Status:** Add menu bar icon or keyboard shortcut to access settings

---

## Testing Requirements

- [ ] Test on macOS 13.0+ (Ventura and newer)
- [ ] Test with multiple monitors
- [ ] Test with different window management apps
- [ ] Test keyboard shortcut conflicts
- [ ] Test memory usage over extended sessions
- [ ] Verify Pro subscription features work correctly

---

## Timeline

**Phase 1:** Planning & Prioritization (Current)  
**Phase 2:** Development (Start after 1.0 approval - 2 weeks)  
**Phase 3:** Internal Testing (1 week)  
**Phase 4:** Beta Testing (Optional - 1 week)  
**Phase 5:** App Store Submission (Same process as 1.0)

**Estimated Total Time:** 4-5 weeks after starting development

---

## Success Metrics

- Improved user ratings on Mac App Store
- Reduced support requests related to addressed issues
- Positive feedback on new features
- No increase in crash rate or bugs
- Maintained or improved performance metrics

---

## Notes

- Keep release focused and small to maintain quality
- Gather user feedback from 1.0 before finalizing feature list
- Consider user requests from support emails and GitHub issues
- Maintain backward compatibility with 1.0 user settings
- All changes should be non-breaking for existing users

---

## Resources Needed

- Development time: ~40 hours
- Testing time: ~10 hours
- Design assets (if needed for button styles): ~2 hours
- Documentation updates: ~2 hours

**Total Estimated Effort:** 54 hours

---

## Open Questions

1. Should we implement telemetry/analytics to better understand feature usage? (Privacy-first approach)
2. Do we need a settings sync feature for users with multiple Macs?
3. Should 1.0.1 include any Pro-only features?
4. What's the minimum version gap before encouraging users to update?

---


## Pre-Release Checklist

Before submitting 1.0.1 to the App Store, verify all core functionality still works:

- [ ] Capture frontmost window still works with default shortcut (⌘⇧6)
- [ ] Pro Monthly/Yearly paywall flow works, no pricing changes
- [ ] Screen Recording permission dialog still appears / works as expected
- [ ] App launches and quits with no new warnings in Console.app
- [ ] OCR and redaction still behave as in 1.0
- [ ] Custom keyboard shortcut (if implemented) works correctly
- [ ] Preview window (if implemented) displays and cancels properly
- [ ] No performance regressions compared to 1.0
- [ ] All automated tests pass
- [ ] Manual testing on macOS 13.0+ (Ventura and newer)

---

## What's New for 1.0.1

_App Store release notes (copy-paste ready):_

### New Features
- **Customizable Keyboard Shortcuts**: Set your own keyboard shortcut for faster captures - no more conflicts with other apps
- **Screenshot Preview**: Optional preview window before copying to clipboard, so you always know what you captured

### Improvements
- **Faster Performance**: Improved capture and OCR processing speed
- **Better Reliability**: Fixed button disappearing on external display disconnect
- **Enhanced Stability**: Optimized first screenshot capture time after app launch

### Bug Fixes
- Fixed issue where button occasionally disappeared when disconnecting external displays
- Fixed settings window accessibility when button was hidden
- Improved app launch performance

_Version: 1.0.1 | Build: TBD | Release Date: TBD_

---

**Last Updated:** December 12, 2024  
**Document Owner:** Development Team  
**Status:** Draft - Open for feedback
