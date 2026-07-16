# ⚽ Football Frenzy

A simple, good-looking three-a-side arcade football (soccer) game that runs in the browser — playable on **PC, tablet and mobile**.

**▶ Play:** https://grigorysolomatov.github.io/football-frenzy/

## The game

- **Three-a-side.** You control the **red** team, the CPU controls **yellow**.
- **Two halves of 3 minutes each**, with a half-time break — just like a real 45'+45' match (scaled down).
- **2D ball physics** — friction, wall bounces, kicks, dribbling and shooting.
- **Steal mechanic:** if you touch an opponent who has the ball for **1 continuous second**, you win possession (a progress ring shows how close you are).

## Controls

The game **auto-selects the red player nearest the ball** (highlighted with a dashed ring), so you only ever steer one player at a time — the rest of your team plays automatically.

| Action | PC | Mobile / Tablet |
|---|---|---|
| Move active player | Move the mouse | Drag your finger on the pitch |
| Kick / shoot / pass | Click, or hold **Space** | Hold the **SHOOT** button |
| Move your goalie | Arrow keys | GK arrow pad (bottom-left) |
| Power | Hold longer = harder | Hold longer = harder |

The ball is kicked **toward your pointer**, so aim where you want it to go. A short tap makes a soft pass; a long hold blasts a shot.

Your goalkeeper is steered separately from your outfield player — using the arrow keys or the on-screen **GK** pad — and stays inside your penalty box. The CPU's goalkeeper always plays automatically.

## AI

Every player — human-team and CPU — uses the **same three actions**: run without the ball, run with the ball (dribble), and shoot. The CPU runs a lightweight role-based system:

- The player nearest a loose ball chases it.
- The ball carrier dribbles toward goal and shoots when in range, or passes to the most advanced open teammate when pressured.
- Off the ball, teammates hold a formation that shifts with play; when defending, the nearest player closes down the carrier while the others drop between the ball and their own goal.

## Tech

A single self-contained `index.html` — vanilla JavaScript, HTML5 Canvas, no build step and no dependencies. Artwork lives in `assets/`.

---
Built with [Claude Code](https://claude.com/claude-code).
