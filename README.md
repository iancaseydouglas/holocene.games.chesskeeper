# Chess Keeper

* **Time Every Move:** Run Bullet, Blitz, Classical, or multi-day matches in digital, hourglass, or analog view.
* **Play Effortlessly:** Start, pause, and switch turns with the spacebar—or automatically on every board move.
* **Sync Anywhere:** Share one screen, float over your desktop, or link two devices in real time without a server. 
* **Track Automatically:** Play on a live, tear-away board that enforces legal moves and writes clean notation for you.
* **Save & Share:** Keep player stats, export Chess.com-ready PGNs, and snap PNG board shots in one click.

### Quick Start

1. **Open the App:** Double-click `index.html` in any modern browser—no installation, Node.js, or server required.
2. **Pick Your Time Control:** Select a preset (Bullet, Blitz, Rapid, Classical, or Epic 1–2 Day) or choose **Custom** in the top bar.
3. **Start & Switch Turns:** Press `Space` to start or pause the clock. To end a turn, either make a move on the floating chessboard (which logs notation automatically) or tap your clock pad / press `Enter`.
4. **Customize Your View:** Switch between **Digital**, **Hourglass**, and **Analog** styles, toggle **Board Only**, **Slim Float**, **Fullscreen (`F`)**, or **Zen Mode (`Z`)**, and save your defaults in **Settings (`⚙`)**.
5. **Link Two Devices (Optional):** Click **2-Device Link** to pair two phones or browsers via **Same Network (P2P)**, **Bluetooth (BLE)**, or zero-login **Epic Cloud Sync (`jsonblob.com`)**.
6. **Save & Export:** Open **Notation** to enter player names, save completed games, and export **Chess.com-ready `.pgn**` files, `.json` backups, or **PNG** snapshots (`📷`).

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
