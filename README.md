# THE-LAST-FLOOR
Game

# The Last Floor

A browser-based 3D first-person stealth/escape game, built as a single `index.html` file.

You are the **imposter** inside Halcyon Tower. Restore the power, take the armory, climb five floors and lift off from the roof by helicopter before the three **hunters** work out who you are. Play solo against AI hunters, or online with friends.

## Features

- First-person 3D gameplay rendered with WebGL (Three.js)
- Five themed floors, each with its own look and rooms
- Stealth mechanic: hunters get suspicious if they see you sprint, shoot, carry a gun, or work with mission objects
- Hiding spots (lockers), noise that travels, a flashlight, and a pistol with ammo and reloading
- Puzzles: wire-matching control panel, keypads, combination notes, lifts
- Three difficulty levels: Easy, Normal, Hard
- Solo mode against three AI hunters
- Online multiplayer lobby (room codes, one imposter and one to three hunters)
- Minimap (unlocked after floor 3), objectives list, health and stamina bars, inventory HUD
- Touch controls for mobile (joystick plus Attack, Use, Jump, Sprint and Item buttons)

## The Floors

| Floor | Name |
|-------|------|
| 1 | Lobby & Utilities |
| 2 | Offices |
| 3 | Executive Floor |
| 4 | Research & Security |
| 5 | Rooftop Level |

## How to Play

1. Find three fuses and restore the power (Floor 1).
2. Get the lift key and take the lift up. Each floor ends with a checkpoint.
3. Collect items, notes and keys along the way (pistol, terrace key, helicopter key, black briefcase, combination note and more).
4. On the roof, unlock the helicopter, fuel it, start the engine and escape.

Check the **Objectives** list (hold `Tab`) to see what is needed on the current floor.

### Controls (keyboard and mouse)

| Key | Action |
|-----|--------|
| `W` `A` `S` `D` | Move |
| `Shift` | Sprint |
| `Space` | Jump |
| `C` | Crouch |
| `E` / `F` | Interact / pick up |
| `G` | Drop suitcase |
| Mouse | Look |
| Click | Shoot |
| `R` | Reload |
| `1` / `2` | Hands / gun |
| `L` | Flashlight |
| `V` | Camera view |
| `P` | Cinematic effects on/off |
| `Tab` | Show objectives |
| `M` | Map (after floor 3) |

Click the game view to capture the mouse. If the browser blocks that, hold the right mouse button to look.

## Online Multiplayer

1. Click **Play with friends**.
2. Enter a username, then either **Create room** or enter a 5-character room code and press **Join**.
3. Share the code with your friend(s), and each player picks a role: Imposter or Hunter.
4. The host presses **Start match**.

Multiplayer uses [PeerJS](https://peerjs.com/) for peer-to-peer connections.

## Running the Game

No build step or installation is needed.

**Option 1:** Double-click `index.html` to open it in your browser.

**Option 2:** Serve it locally (recommended, works the same in Git Bash or WSL):

```bash
python -m http.server 8000
```

Then open <http://localhost:8000> in your browser.

> An internet connection is required, because the game loads libraries and fonts from CDNs (see below).

## Tech Stack

- HTML, CSS and vanilla JavaScript (everything lives in one file)
- [Three.js r128](https://threejs.org/) with post-processing (bloom, ambient occlusion) and the Reflector object
- [PeerJS 1.5.4](https://peerjs.com/) for online play
- Google Fonts: Barlow Condensed and Special Elite

## Project Structure

```
.
├── index.html   # The whole game: markup, styles and scripts
└── README.md    # This file
```

## Tips

- Walk instead of sprinting near hunters. They grow suspicious of suspicious behavior.
- Lockers hide you, and noise travels, so move carefully.
- Hunters can hurt you, so keep an eye on your health bar.
