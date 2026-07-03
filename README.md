# Magnum Force Online — Classic Maze Edition

A GitHub Pages deployable online room-code prototype with a denser, more original-feeling city board.

## What changed in this version

- Fixed handcrafted **25 x 25** board
- **Single-tile street corridors** between buildings
- Denser maze-like city layout
- Distinct building graphics by type:
  - hospital
  - bullet shop
  - police station
  - hotel / tower
  - bank / office
  - club / safe house
  - warehouse / garage
- Multiple marked **green doors**
- Structures can only be entered or exited through doors
- You cannot enter and leave the same structure in one turn
- Multiple **manholes** teleport players across the city
- Firebase online room-code play

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
