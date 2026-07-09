# The Scratch Bugs & Tricks Hub

Welcome! This is an open-source, community-driven guide tracking common Scratch bugs, limits, quirks, and the clever tricks used to work around them.

No coding experience is required to contribute. If you know a repeatable Scratch issue and a practical fix, you can add it here.

## Current Bugs & Tricks Tracker

| # | Bug or constraint | Quick trick | Full entry |
|---|---|---|---|
| 1 | The 300-clone limit | Reuse clones, delete off-screen clones, and switch dense effects to stamped/costume-based rendering. | [entries/300-clone-limit.md](entries/300-clone-limit.md) |
| 2 | Clone setup race | Store clone settings before creating the clone, then let the clone read them immediately on start. | [entries/clone-setup-race.md](entries/clone-setup-race.md) |
| 3 | Broadcast storms | Gate repeated broadcasts with state variables or cooldowns. | [entries/broadcast-storms.md](entries/broadcast-storms.md) |
| 4 | Cloud variable data limits | Encode compactly, split records, and update only when values change. | [entries/cloud-variable-limits.md](entries/cloud-variable-limits.md) |

## Earn a Promotion to Moderator

I am looking for co-leaders to help manage this growing repository. Contributors should start by submitting high-quality pull requests using the template below. Trusted contributors can be promoted to repository moderators, who may review community submissions and commit approved fixes directly when repository permissions allow it.

## Contributor Template

When adding a bug or trick, copy this format into a new file under `entries/`:

```md
# [Name of the Bug or Engine Constraint]

**The Issue:** [What goes wrong or stops working?]

**The Trick:** [Explain in clear English step-by-step how to set up the blocks or logic to fix it.]

**Best For:** [What kinds of Scratch projects benefit from this?]

**Watch Out For:** [Any tradeoffs, limits, or mistakes to avoid.]

**Contributed by:** [@YourGitHubUsername]
```

Then add a row for your entry in the tracker table above.

## Good Entry Checklist

- The issue can be reproduced in Scratch.
- The trick uses clear steps a beginner can follow.
- The entry names any tradeoff, such as lag, memory use, or project complexity.
- The entry does not promise "infinite" objects, storage, speed, or multiplayer unless it explains the real limit.

Maintained by [@randomperson208](https://github.com/RandomPerson208). Use the template, share your fixes, and help make Scratch debugging less mysterious.
