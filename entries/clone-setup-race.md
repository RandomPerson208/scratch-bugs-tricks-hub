# Clone Setup Race

**The Issue:** A clone sometimes starts running before it has the position, costume, health, speed, or type you expected. This can make clones flash in the wrong place or behave like the previous clone.

**The Trick:** Set the clone's setup data before creating it, then let the clone copy that data immediately.

1. In the original sprite, set temporary variables such as `spawn x`, `spawn y`, `spawn costume`, and `spawn speed`.
2. Create the clone.
3. In `when I start as a clone`, immediately move to `spawn x` and `spawn y`.
4. Copy shared setup values into clone-local variables, such as `my speed` or `my type`.
5. Only show the clone after the setup is complete.

**Best For:** Enemy spawners, bullets with multiple types, particle systems, and collectible items.

**Watch Out For:** If several sprites create clones at the same time, shared setup variables can be overwritten. Use separate setup variables per sprite or make each spawner responsible for only one clone family.

**Contributed by:** @randomperson208
