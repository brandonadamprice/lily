# 🦄 Unicorn Quest: The Lost Magic

A gentle platformer for little players (ages ~4+). Lily the unicorn's magic is
scattered across **10 lava lands** — win each level to earn a piece of her
magic back!

## Play it

🎮 **[unicorngame.hallowedgains.com](https://unicorngame.hallowedgains.com)**

Served straight from this repo by GitHub Pages — every push to `main` goes
live within a minute or so.

### Install it as an app

Unicorn Quest is a PWA, so it can live on a home screen like a real app —
its own icon, no browser bars, and it works with no internet at all.

- **Android / Chrome / Edge** — an **📲 Install Unicorn Quest** button appears
  on the title screen (the browser menu has "Install" too)
- **iPhone / iPad** — tap **Share** ⬆️ then **Add to Home Screen** (Safari has
  no install button; the title screen shows a reminder)
- **Desktop Chrome / Edge** — the install icon at the right of the address bar

Once installed it opens fullscreen in landscape and plays offline. Saved magic
is kept by the browser, so it carries over from the website to the installed
app on the same device.

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
- Hearts! Little hearts pop out when Lily flutters, grabs a star or wins a
  level, they trail behind her gallop once Sparkle Trail is unlocked, and tiny
  ones twinkle away in the sky
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

Everything (graphics, sounds, music, levels) is generated in code — the whole
game is one HTML file with no dependencies. The other files are just the app
wrapper: `manifest.json` describes the installed app, `sw.js` caches the game
for offline play, and the four icons are rendered by the game's own unicorn
drawing code (`node tools/make-icons.mjs` re-makes them).

The service worker fetches the page from the network first and falls back to
its cache, so a push to `main` is still live on the next launch — the cache is
only there for when the network isn't. `sw.js` carries a panic switch in its
header comment if it ever needs to be turned off.

## The cutesy look

Everything the player reads sits on a pastel-pink card: polka-dot paper, a
white ring with a candy-pink halo, dashed "sticker" buttons, glowing candy
pills for the level/star counters, and hearts, sparkles and bows drifting up
behind the card. The play controls fade politely out of the way whenever a
card is on screen.

## Fonts

The game pins two Google Fonts so it looks the same on every device:

- **Pacifico** — the cursive script used for big titles ("Unicorn Quest",
  "Level complete!")
- **Fredoka** — the round, bubbly font used for everything else, chosen so the
  HUD, buttons and hints stay easy for a new reader (Baloo 2 is kept next in
  the stack as a near-identical fallback)

Before this was pinned, the CSS was a fallback *chain* (`'Comic Sans MS',
'Chalkboard SE', … cursive`), so each device stopped at whichever font it
happened to have — Comic Sans on Windows, a script face on phones. That is why
the game used to look different on mobile and desktop.

Playing offline by double-clicking the file still works; without a network the
web fonts simply fall back to that old system stack.
