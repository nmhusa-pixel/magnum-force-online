# Magnum Force Online — Original Style Map Edition

This is a GitHub Pages-deployable online room-code version of Magnum Force with a larger original-style city board.

## New map features

- Larger 21 x 21 board
- Larger multi-tile hospitals
- Larger multi-tile bullet shops
- Larger named buildings
- Buildings have marked green doors
- Structures can only be entered and exited through doors
- You cannot enter and leave the same structure in one turn
- Multiple manholes teleport agents across the game map
- Fixed and card-placeable road blocks
- Online multiplayer rooms through Firebase Realtime Database

## Files

- `index.html` — complete static browser game
- `README.md` — setup notes

## Firebase rules for testing

In Firebase Console:

**Build → Realtime Database → Rules**

Use this for initial testing only:

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

For public release, replace this with stricter rules and Firebase Authentication.

## Deploy on GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and `README.md`.
3. Go to **Settings → Pages**.
4. Choose **Deploy from a branch**.
5. Select `main` and `/root`.
6. Save.

## How to play online

1. Player 1 opens the game and clicks **Create Room**.
2. Share the room code.
3. Other players open the same URL, enter the room code, and click **Join Room**.
4. Each player clicks **Take Seat** for an agent.
5. Only the current seated agent can move, shoot, use cards, or end the turn.
