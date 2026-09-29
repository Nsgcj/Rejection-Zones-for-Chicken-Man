# Bolt's Journal - Critical Learnings

## 2025-09-29 - Pine Script Array Search Optimization
**Learning:** In Pine Script v6, searching global arrays chronologically populated during historical bar processing (such as active zones or swing levels) can be optimized from O(N) to O(1) by iterating backwards from `array.size() - 1 to 0` and breaking early once the timestamp or sequence key predates the target window.
**Action:** Always prefer reverse iteration with early break for time-ordered arrays in Pine Script.
