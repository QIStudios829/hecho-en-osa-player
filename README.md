# Hecho en Osa Player

A retro music player with live visualizers, a Surfer vs Shark game and a dancing QR code, made for **Hecho en Osa**: a free 8-week hackathon and science fair for young builders, ages 11 to 17, on the Osa Peninsula, Costa Rica, run by The Gift Academy.

**Built by Trent Simpson, Mentor · Hecho en Osa 2026**

- Live player: https://hechoenosaplayer.netlify.app
- Hecho en Osa: https://thegift.is/hechoenosa

## What it does

- Plays the Hecho en Osa playlist: Spark Night, Vibe Jam Hecho en Osa, Code Freeze Fiesta, Before It Was Real
- 10-band equalizer with presets
- 7 visualizers that react to the music, named after hackathon milestones: Spark Night, Vibe Jam, Build Week, Bug Hunt, Code Freeze, Ship It, Exhibition Day
- **Surfer vs Shark** in the background. Pick EVADE to be the surfer or CHOMP to be the shark, then move with your mouse, finger or arrow keys
- A QR code in the corner that dances to the beat and links to the Hecho en Osa site
- Drag in your own music with **+ ADD YOUR OWN MUSIC**

## Run it yourself

No installs and no build step. Everything is in one file: `index.html`.

1. Download this repo (green **Code** button, then **Download ZIP**) and unzip it.
2. Open `index.html` in your browser. The songs play right away.
3. To make the visualizers and EQ work on your own computer, serve the folder instead of opening the file:

   ```bash
   python3 -m http.server 8000
   ```

   Then go to http://localhost:8000

## Add a song

1. Put the mp3 in the `songs/` folder.
2. In `index.html`, find `const PLAYLIST = [` and add a line like the ones already there:

   ```js
   { title: 'My Song', dur: '2:30', secs: 150, src: 'songs/my-song.mp3', bitrate: 192, sample: 44 },
   ```

## How it's built

- Plain HTML, CSS and JavaScript. No frameworks.
- The **Web Audio API** reads the music, and the visualizers and the bouncing QR code use that data.
- The visualizers, the game and the QR code are drawn on an HTML `canvas` or with SVG.
- Started from the AGDAMP player built for *Adventures of Gradient Descent*, then remixed for Hecho en Osa.
- Vibe coded with Claude Code.

Got a song, game or puzzle you wanna make? Turn your idea into something real. Build it. Show it. Win.

## Credits

Hecho en Osa is The Gift Academy's event and brand. Player by Trent Simpson, Mentor.
