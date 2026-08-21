# 🦄 Unicorn Quest: The Lost Magic

A gentle platformer for little players (ages ~4+). Lily the unicorn's magic is
scattered across **10 lava lands** — win each level to earn a piece of her
magic back!

## Play it

🎮 **[unicorngame.hallowedgains.com](https://unicorngame.hallowedgains.com)**

Served straight from this repo by GitHub Pages — every push to `main` goes
live within a minute or so.

## How to play

You can also just open [index.html](index.html) in any browser — double-click
it, no install or internet needed.

- **⬅ ➡** (or A/D) — run
- **⬆ / Space** (or W) — jump
- Press jump **again in the air** to do a magic flutter (double jump)
- Big on-screen buttons work too (mouse or touch)
- After winning a level, press **Space** (or Enter) to jump straight to the
  next one — no mouse needed
- **Esc** (or the ⏸ button) pauses — keep playing, restart the level, or go
  back to the level map
- 🔊 button (top right) mutes the music and sounds
- Bump into a butterfly and it flutters out of the way!
- **Friendly lava sharks** patrol below — fins cutting the surface, leaping in
  big arcs. Bump one mid-leap and it boops Lily up for a bonus bounce (they
  are never dangerous)
- Land on a smiley **trampoline flower** for a super bounce (level 2+)
- Collect **every star** in a level for a PERFECT ⭐ badge on the level map
- Watch for the friendly lava fish leaping in the background
- Colorful little birds fly past in V formations — and some magic ones trail
  fairy dust behind them
- Two ranges of animated volcanoes smoke, glow, drip lava, and erupt on their
  own rhythms
- A **day-night cycle** rolls through midday, sunset, a starry night, and dawn
  every ~3 minutes — a smiley sun and sleepy moon arc across the sky, stars
  twinkle after dark, and shooting stars streak past. Each level starts at a
  different time of day
- Beating level 10 triggers a grand finale: Lily flies a rainbow
  loop-the-loop with fireworks!

## The 10 magic unlocks

| Level | Magic |
|-------|-------|
| 1 | ✨ Sparkle Trail |
| 2 | 🌈 Rainbow Mane |
| 3 | 🦋 Butterfly Friends |
| 4 | 🧲 Star Magnet |
| 5 | 💫 Triple Flutter |
| 6 | 🪽 Magic Wings — hold JUMP in the air to glide! |
| 7 | 🦘 Super Bounce |
| 8 | 🌠 Glitter Gallop |
| 9 | 👑 Star Crown |
| 10 | 🔮 ALL the Magic! |

Progress is saved in the browser (localStorage), so unlocked magic sticks
between play sessions. The title screen has a tiny "start my magic over" link
(with a confirmation) to reset.

## Kid-friendly by design

- **You can't lose.** Falling into the lava just summons a friendly rescue
  cloud that carries you back to the last island you stood on.
- Generous jumps, coyote time, and the flutter double-jump make the gaps easy.
- Levels get gently longer and trickier (moving islands appear from level 3),
  but every level stays well within easy jump range.
- Collecting stars is optional — reaching the crystal always wins.
- Night only dims the sky and background — the islands, stars, and Lily stay
  bright and easy to see.

Everything (graphics, sounds, music, levels) is generated in code — it's a
single HTML file with no dependencies.

## Fonts

The game pins two Google Fonts so it looks the same on every device:

- **Pacifico** — the cursive script used for big titles ("Unicorn Quest",
  "Level complete!")
- **Baloo 2** — the rounded font used for everything else, chosen so the HUD,
  buttons and hints stay easy for a new reader

Before this was pinned, the CSS was a fallback *chain* (`'Comic Sans MS',
'Chalkboard SE', … cursive`), so each device stopped at whichever font it
happened to have — Comic Sans on Windows, a script face on phones. That is why
the game used to look different on mobile and desktop.

Playing offline by double-clicking the file still works; without a network the
web fonts simply fall back to that old system stack.
