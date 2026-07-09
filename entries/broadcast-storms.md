# Broadcast Storms

**The Issue:** A broadcast sent inside a fast loop can trigger many scripts at once. Projects may lag, repeat sounds, spawn too many clones, or run the same logic many times in a frame.

**The Trick:** Add a gate so the broadcast only fires when the state changes or when a cooldown finishes.

1. Create a variable such as `can broadcast?` or `last state`.
2. Before sending the broadcast, check whether the event is actually new.
3. After broadcasting, set the gate to closed.
4. Open the gate again when the player releases a key, the animation finishes, or a short cooldown expires.
5. For repeated events, use `broadcast and wait` only when later logic must wait for every receiver to finish.

**Best For:** Menus, attacks, sound effects, level transitions, and button/key input.

**Watch Out For:** `broadcast and wait` can make a project feel frozen if one receiving script contains a long loop. Use regular `broadcast` when receivers can run independently.

**Contributed by:** @randomperson208
