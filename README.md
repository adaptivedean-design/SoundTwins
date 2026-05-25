# Sound Twins

Sound Twins is a static phonics review game for matching two word pairs that share the same sound.

## Play

Open `index.html` in a browser, or host this repository with GitHub Pages.

## Teacher Links

The teacher setup screen can create a player link. The link stores the selected sound families, round count, timer, and celebration setting in the URL so a student can open the game remotely with the same settings.

## Live Rooms

The teacher setup screen can also create a Firebase live room. In a live room, the player joins with the generated link, clicks Ready, and waits for the teacher to start. The teacher can observe the player status, current cards, and progress, then reset the room when needed.

The teacher can click a word card in the observer view to briefly spotlight the same card on the player's screen.

For first testing, the Firebase Realtime Database needs rules that allow room reads and writes. A simple testing rule is:

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

These rules are suitable for early testing, not private student data.
