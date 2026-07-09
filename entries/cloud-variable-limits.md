# Cloud Variable Data Limits

**The Issue:** Cloud variables are useful for shared scores and project data, but they have strict limits on format, size, number of variables, and update rate. Large save systems can fail, lag, or overwrite data unexpectedly.

**The Trick:** Store only compact numeric data and update it carefully.

1. Save the smallest useful record, such as score, level, time, or encoded inventory.
2. Convert text or choices into numbers before saving.
3. Split longer records across multiple cloud variables only when needed.
4. Update cloud variables only when the value changes.
5. Keep a local variable copy so the project can still run if cloud data is delayed.

**Best For:** High scores, simple leaderboards, small multiplayer signals, and shared counters.

**Watch Out For:** Cloud variables are not private storage. Do not save personal information, passwords, chat messages, or anything that should be secret.

**Contributed by:** @randomperson208
