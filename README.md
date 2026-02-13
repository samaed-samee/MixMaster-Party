# MixMaster Party

**The ultimate party game challenge** - A real-time multiplayer party game with voice chat, built for the browser.

![Game Preview](https://img.shields.io/badge/status-active-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue)

---

## Features

- **4 Exciting Game Modes:**
  - **Truth or Dare** - Classic secrets and challenges
  - **Never Have I Ever** - Confess your past experiences
  - **Would You Rather** - Impossible choices and hilarious debates
  - **Categories** - Fast-paced word association game

- **Real-Time Multiplayer:**
  - Create or join rooms with 4-character room codes
  - Support for 2 players per room
  - P2P encrypted connections using WebRTC

- **Voice Chat:**
  - Built-in voice communication
  - Mute/unmute controls
  - Visual mute status indicators

- **Modern UI/UX:**
  - Sleek dark theme with gradient accents
  - Responsive design for all devices
  - Smooth animations and transitions
  - Toast notifications for game events

---

## How to Play

### Setup
1. Open `game.html` in a modern web browser (Chrome, Firefox, Edge, Safari)
2. Enter your name in the text field
3. Choose to either:
   - **Create New Room** - You'll be the host
   - **Join a Room** - Enter a 4-character room code from the host

### Gameplay
1. In the lobby, all players can see who's joined
2. The host selects a game mode
3. Random prompts appear on screen
4. The active player (randomly selected) must complete the challenge
5. Host clicks "Next Challenge" to continue

### Voice Chat
- Click the microphone icon to enable/disable your mic
- Mute status is shown to all players
- Voice chat works automatically when mic is enabled

---

## Technical Details

### Technologies Used
- **React 18** - UI framework
- **Tailwind CSS** - Styling
- **PeerJS** - WebRTC wrapper for P2P connections
- **Lucide Icons** - Icon library
- **Babel Standalone** - JSX transformation in browser

### Architecture
- **Single-file application** - Everything in one HTML file for easy deployment
- **P2P networking** - No server required (except for STUN/TURN)
- **State synchronization** - Room state broadcast from host to guests
- **Real-time audio** - WebRTC media streams for voice chat

### Networking
- Uses Google STUN servers for NAT traversal
- TURN servers configured for reliable connections (openrelay.metered.ca)
- Host acts as the authoritative state source
- Automatic reconnection handling

---

## Browser Compatibility

- Chrome 80+
- Firefox 76+
- Safari 14+
- Edge 80+

**Note:** Requires HTTPS or localhost for microphone access (browser security requirement).

---

## Deployment

### GitHub Pages
1. Push this repository to GitHub
2. Go to repository Settings → Pages
3. Select main branch as source
4. Your game will be live at: `https://samaed-samee.github.io/mix-master/`

### Other Hosting Options
- **Netlify/Vercel** - Drag and drop the HTML file
- **Any static hosting** - Just upload `game.html`

---

## Project Structure

```
mix-master/
├── game.html          # Complete game (single file)
└── README.md          # This file
```

---

## Known Limitations

- Maximum 2 players per room (can be increased by changing `MAX_PLAYERS` constant)
- Requires stable internet connection for P2P
- Some corporate networks may block WebRTC
- TURN server credentials are public (for demo purposes only)

---

## Future Enhancements

- [ ] Increase max players to 4-8
- [ ] Add more question banks
- [ ] Custom game mode creation
- [ ] Score tracking
- [ ] Game history/replay
- [ ] Mobile app wrapper (React Native)
- [ ] Dedicated TURN server setup

---

## Credits

Built with React, Tailwind CSS, and PeerJS.

**Developer:** [samaed-samee](https://github.com/samaed-samee)

---

## License

MIT License - feel free to use, modify, and distribute!

---

## Support

Found a bug or have a feature request? Open an issue on GitHub!

---

*Made with lots of coffee and late-night coding sessions.*