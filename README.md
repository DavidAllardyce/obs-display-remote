# Church OBS Remote Control & Projector Launcher

A lightweight, web-based remote control interface and projector launcher for **OBS Studio** built specifically for church media teams, live streaming, and presentation environments. 

It connects directly to OBS Studio over WebSockets (v5 API), allowing team members to switch scenes seamlessly and trigger fullscreen/windowed projectors on the host computer from any phone, tablet, or laptop on the local network.

---

## 🌟 Features

- **📱 Mobile-Friendly & PWA Ready**: Optimized for touchscreens (phones & tablets) with double-tap prevention and mobile home screen PWA installation support.
- **🔴 Real-Time Scene Switching**: View live status indicator badges (`LIVE` / `PREVIEW`) and tap to switch active OBS scenes instantly with optimistic UI updates.
- **🖥️ Remote Projector Launcher**: Remotely launch OBS Video Mix Projectors (Program or Preview) in full-screen or windowed mode across multi-monitor setups directly from the remote interface.
- **⚡ Persistent Credentials & Auto-Connect**: Remembers your OBS IP address and password in browser storage, automatically reconnecting on startup.
- **🔄 Auto-Reconnection & Live Status**: Visual connection status badge with automatic background reconnection retries if network connectivity drops.
- **🛠️ Zero Build Setup**: Pure client-side web application. No server installation, Node.js environment, or build pipeline required!

---

## 🚀 Quick Start

### 1. Enable WebSocket Server in OBS Studio
1. Open **OBS Studio** (v28.0+ includes WebSocket v5 natively).
2. Go to **Tools** ➔ **WebSocket Server Settings**.
3. Ensure **Enable WebSocket server** is checked.
4. Note your **Server Port** (default is `4455`) and your **Server Password** (if configured).

### 2. Launch the Remote Interface
- Open [`index.html`](index.html) in any modern web browser on a device connected to the same local network as the OBS host computer.
- *(Optional)* Serve the project folder using any local HTTP server (e.g. `npx serve` or Python's `python -m http.server 8000`).

### 3. Connect to OBS
1. Enter the local IP address and port of the computer running OBS (e.g. `192.168.1.50:4455`).
2. Enter your WebSocket Password (if set).
3. Click **Connect**.

---

## 💻 Tech Stack

- **HTML5 & Vanilla JavaScript (ES6)**
- **Tailwind CSS** (via CDN for dark-mode interface styling)
- **obs-websocket-js** (OBS WebSocket v5 client library)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
