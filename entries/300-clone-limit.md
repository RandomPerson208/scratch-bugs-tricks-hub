# The 300-Clone Limit

**The Issue:** Scratch stops creating new clones once the project reaches the active clone limit. This can break particle effects, bullet patterns, platformer tiles, scrolling worlds, and enemy spawners.

**The Trick:** Treat clones like a limited pool instead of disposable objects.

1. Give each clone a job, such as bullet, particle, enemy, or tile.
2. When a clone leaves the screen or finishes its animation, hide it and mark it as available.
3. Reuse an available clone by changing its position, costume, direction, and variables.
4. Delete clones you truly no longer need with `delete this clone`.
5. For very dense visuals, replace some clones with pen/stamp effects, costume changes, or a smaller set of larger sprites.

**Best For:** Shooters, particle effects, scrolling maps, platformers, and games with many repeated objects.

**Watch Out For:** Clone pooling is more complex than simple `create clone of myself` scripts. Keep a variable such as `active?` or `mode` so hidden clones do not keep running collision or movement code.

**Contributed by:** @randomperson208
