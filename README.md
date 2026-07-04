# Magnum Force Online — Refined Classic Maze Edition

A GitHub Pages deployable online room-code game with a tighter classic board-game feel.

## Improvements in this version

- Tighter single-tile street corridors
- Denser handcrafted 25 x 25 maze map
- More retro printed-board styling
- Distinct graphics by building type
- Larger hospitals and bullet shops
- Green door entry/exit rules
- Selectable manhole destinations
- Cleaner agent dashboard with ammo and wound meters
- Improved card display
- Firebase room-code multiplayer

## Files

- `index.html`
- `README.md`

## Firebase rules for testing

In Firebase Console:

**Build → Realtime Database → Rules**

Use this during testing:

```json
{
  "rules": {
    "rooms": {
      "$roomId": {
        ".read": true,
        ".write": true
      }
    }
  }
}
```

For public release, tighten rules and add Firebase Authentication.

## GitHub Pages deploy

1. Create a new GitHub repository.
2. Upload `index.html` and `README.md`.
3. Open **Settings → Pages**.
4. Choose **Deploy from a branch**.
5. Select `main` and `/root`.
6. Save.

## Online play

1. Player 1 clicks **Create Room**.
2. Share the room code.
3. Other players click **Join Room**.
4. Each player clicks **Take Seat** for an agent.
5. Only the current seated agent can act on that turn.
