# Pure Chess Clock — by Holocene Games

A **zero-dependency, single-page HTML5 / CSS3 / vanilla JavaScript** chess clock with an integrated floating chessboard, algebraic notation scorecard, PGN game archive, and 2-device synchronization.

No Node.js, no `npm install`, no build step, and no external CDN assets required—open `index.html` in any modern browser and play.

## Features & Clock Styles

- **Three Clock Styles**
  - **Digital**: Ultra-large `tabular-nums` countdown with tenths-of-a-second precision under 20 seconds.
  - **Hourglass**: Animated dual-chamber SVG hourglass with proportional sand levels and falling sand stream.
  - **Analog**: Classic tournament-style clock face with sweeping minute/second hands and a low-time flag indicator.
- **Layout & Display Modes**
  - **Standard Split**: Full-width dual player pads.
  - **Fullscreen (`F`)**: Edge-to-edge distraction-free display.
  - **Slim Float**: Draggable, compact horizontal bar for desktop use.
  - **Dark & Light Themes (`T`)**: High-contrast dark slate and warm tournament ivory palettes.
  - **Symbols-Only Button View**: Toggle button labels off to display clean symbol icons only.
- **Settings & Saved Defaults**
  - Open the **Settings (⚙)** modal to set and persist your preferred defaults for theme, clock style, time control, spacebar behavior, piece style, button view, board flyout, notation mode, and sound.

## Game Modes

### 1. Single-Device Mode
Both players share one screen. Tap your clock pad or press `Enter` to end your turn and add any configured increment. Press `Space` to turn the clock on and off (or switch `Space` to turn-switching in the bottom bar or Settings).

### 2. Floating Chessboard & Notation Mode
- **Floating Chessboard (Default: On)**: A draggable mini-board that enforces legal chess rules (castling, en passant, promotion, check/checkmate). Making a move on the board automatically generates Standard Algebraic Notation (SAN), logs it to the scorecard, and switches the clock turn.
- **Piece Styles**: Choose between **Staunton 3D**, **Staunton Classic**, and **Flat Chess Book**.
- **Notation & Saved Games**: Toggle **Notation** to enter custom **White** and **Black** player names, record or edit moves, save completed games locally, and copy or download `.pgn` files.

### 3. 2-Device Link Mode (Two Phones / Two Screens)
Each player keeps their own clock and their own board oriented to their side (**My Side: White** or **My Side: Black**), and every clock action and board move syncs in real time.

#### How to Connect Two Devices
1. Open `index.html` on both devices and click **2-Device Link** in the top bar.
2. Choose **My Side: White** on one device and **My Side: Black** on the other (the board automatically flips to match your side).
3. Pick one of the three built-in connection methods:
   - **Same Network (P2P via WebRTC — Serverless)**:
     1. Player 1 clicks **1. Create Invite Code** and copies the generated code.
     2. Player 2 pastes it into *Paste Other Player's Code Here* and clicks **2. Accept Invite & Create Reply**, then sends the reply code back.
     3. Player 1 pastes the reply code and clicks **3. Complete Connection**. Both clocks and boards are now linked directly peer-to-peer.
   - **Bluetooth (BLE via Web Bluetooth API)**:
     - Click **Scan & Pair Bluetooth Device** in Chrome/Edge (HTTPS or `localhost`) to connect to a compatible BLE GATT UART peripheral/bridge (`6e400001-b5a3-f393-e0a9-e50e24dcca9e`). *(Note: standard web browsers act as BLE centrals and cannot advertise as a GATT peripheral directly to another browser without a BLE bridge/device; use Same Network P2P for direct browser-to-browser play.)*
   - **Same-Browser Tab (`BroadcastChannel`)**:
     - Enter a room name (e.g. `chess-room-1`) and click **Join Room** in two tabs of the same browser to test two-sided play immediately.


### 4. Board-Only Mode (Timed or Untimed)
Click **Board Only** in the top bar to expand the chessboard into the main play area for casual or over-the-board play. Toggle **Clock: On** to automatically switch the compact White/Black clocks on every board move, or **Clock: Off (Untimed)** to play purely on the board with no timer.

## Keyboard Shortcuts

| Key | Action |
| --- | --- |
| `Space` | Turn clock On / Off (configurable to Switch Turn) |
| `Enter` | Switch Turn |
| `R` | Reset Clock & Board |
| `T` | Toggle Dark / Light Theme |
| `F` | Toggle Fullscreen |

## License

Released under the [MIT License](LICENSE).
