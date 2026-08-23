# Church OBS Remote Control & Dual-Display Projector Launcher

A lightweight, mobile-friendly web remote control interface and multi-monitor projector launcher for **OBS Studio** built specifically for media teams, houses of worship, live streaming, and presentation environments.

It connects directly to OBS Studio over WebSockets (v5 API), allowing team members to remotely control scenes, toggle **Studio Mode**, transition preview to live program, and launch fullscreen displays for both **Audience** and **Back of House** monitors.

---

## 🌟 Features

- **📱 Mobile-Friendly & PWA Ready**: Optimized for touchscreens (phones & tablets) with double-tap prevention and mobile home screen PWA installation support.
- **🖥️ Dual-Display Remote Launcher**: Launch and configure fullscreen projectors for **Audience** (Program output) and **Back of House** (Preview, Multiview, or Program) on specific monitors with a single tap.
- **🎬 Studio Mode Integration**: Toggle Studio Mode remotely over WebSocket and perform smooth transitions (`Preview ➔ Live`) with a dedicated Cut/Transition control bar.
- **🔴 Dual Preview & Program Badging**: Real-time visual status badges (`LIVE` in red, `PREVIEW` in green) for instant feedback across team devices.
- **⚡ Persistent Credentials & Preferences**: Remembers your OBS IP address, password, and target monitor assignments in browser storage (`localStorage`).
- **🔄 Auto-Reconnection & Live Status**: Visual connection status badge with automatic background reconnection retries if network connectivity drops.
- **🛠️ Zero Build Setup**: Pure client-side web application. No server installation, Node.js environment, or build pipeline required!

---

## 🚀 Dual Display & Studio Mode Workflow

1. **Audience Display (Screen 1)**: Configured to project `OBS_WEBSOCKET_VIDEO_MIX_TYPE_PROGRAM` onto your main projector/display.
2. **Back of House Display (Screen 2)**: Configured to project `OBS_WEBSOCKET_VIDEO_MIX_TYPE_PREVIEW` or `OBS_WEBSOCKET_VIDEO_MIX_TYPE_MULTIVIEW` for camera operators and control room monitors.
3. **Studio Mode Operations**:
   - Turn **Studio Mode** ON from the top bar.
   - Tap any scene card or **Stage Preview** to cue a scene for Back of House review without affecting the Audience display.
   - Tap **TRANSITION PREVIEW ➔ LIVE** to fade or cut the staged scene to the Audience display.

---

## 💻 Quick Start

### 1. Enable WebSocket Server in OBS Studio
1. Open **OBS Studio** (v28.0+ includes WebSocket v5 natively).
2. Go to **Tools** ➔ **WebSocket Server Settings**.
3. Ensure **Enable WebSocket server** is checked.
4. Note your **Server Port** (default is `4455`) and your **Server Password** (if configured).

### 2. Launch the Remote Interface
- Open [`index.html`](index.html) in any modern web browser on a device connected to the same local network as the OBS host computer.
- *(Optional)* Serve the project folder using any local HTTP server (e.g. `npx serve` or Python's `python -m http.server 8000`).

### 3. Connect to OBS & Launch Displays
1. Enter the local IP address and port of the computer running OBS (e.g. `192.168.1.50:4455`).
2. Enter your WebSocket Password (if set) and click **Connect**.
3. Under **Dual Display & Projector Launcher**, select your target monitor for Audience and Back of House, then click **🚀 LAUNCH BOTH DISPLAYS**.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
