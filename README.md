# 🎯 Tarkov Pilot Sync

<div align="center">

![Tarkov Pilot Sync](https://img.shields.io/badge/Tarkov%20Pilot-Sync-f59e0b?style=for-the-badge&logo=googlechrome&logoColor=white)
![Version](https://img.shields.io/badge/version-3.0.0-blue?style=for-the-badge)
![License](https://img.shields.io/badge/license-GPL--3.0-green?style=for-the-badge)

**Extends Tarkov Pilot to sync player positions, pins, and quests between multiple users on tarkov-market.com**

[Report Bug](#-how-to-report-a-bug) · [Request Feature](https://github.com/DooDesch/TarkovPilotSync/issues/new?labels=enhancement&template=feature_request.md) · [Roadmap](ROADMAP.md)

</div>

---

## 📖 About

Tarkov Pilot Sync is a Chrome extension that enhances your Escape from Tarkov planning experience by allowing you to:

- 🗺️ **Sync player positions** in real-time with your squad
- 📍 **Share map pins** with CTRL+Click
- 📋 **Track quests** together with teammates
- 🔔 **Get notifications** when players join, leave, or change maps
- 📸 **Screenshot Sync** - Automatically detect in-game screenshots and sync your position to tarkov-market.com

### 📸 Screenshot Sync Feature

The Screenshot Sync feature monitors your Tarkov screenshots folder and automatically sends your in-game position to tarkov-market.com.

#### Connection Modes

**Option A: Desktop App (Recommended)**
1. Verify you're on [Tarkov Pilot Desktop App](https://tarkov-market.com/pilot) Mode
2. **Connect your Screenshots folder** in the extension settings
3. **Take a screenshot in-game** (default: PrintScreen)
4. Your position appears on the map within milliseconds!

**Option B: Hook ID (Manual Setup)**
1. **Get your Hook-ID** from [tarkov-market.com/pilot](https://tarkov-market.com/pilot)
2. Enter the Hook-ID in the extension settings (Screenshot Sync → Connection Mode → Hook ID)
3. **Connect your Screenshots folder**
4. **Take a screenshot in-game** (default: PrintScreen)
5. Your position appears on the map (may take a few seconds, based on tarkov-market API response time)!

> 💡 **Tip:** Grant permanent folder access ("Allow on every visit") to avoid re-authorizing after browser restarts.

Perfect for coordinating raid strategies with your squad!

---

## 🐛 How to Report a Bug

Found a bug? Help us fix it by following these steps:

### Step 1: Download Debug Logs

Debug logs contain valuable information that helps us identify and fix issues quickly.

1. **Open the Extension Options**
   - Right-click the Tarkov Pilot Sync icon in your browser toolbar
   - Click "Options" or go to `chrome://extensions` → Tarkov Pilot Sync → Details → Extension options

2. **Navigate to Advanced Settings**
   - Scroll down to the "Advanced Settings" section

3. **Download the Logs**
   - Click the **"Download Debug Logs"** button
   - A JSON file will be downloaded: `tarkov-pilot-sync-logs-YYYY-MM-DD.json`

> 💡 **Tip:** Enable "Debug Mode" before reproducing the bug to capture more detailed logs!

### Step 2: Create an Issue

1. **Go to the Issues page**
   - [Create New Issue](https://github.com/DooDesch/TarkovPilotSync/issues/new)

2. **Use this template:**

```markdown
## Bug Description
A clear and concise description of what the bug is.

## Steps to Reproduce
1. Go to '...'
2. Click on '...'
3. See error

## Expected Behavior
What you expected to happen.

## Actual Behavior
What actually happened.

## Screenshots
If applicable, add screenshots to help explain your problem.

## Environment
- Extension Version: [e.g., 3.0.0]
- Browser: [e.g., Chrome 120]
- OS: [e.g., Windows 11]

## Debug Logs
[Attach your debug log file here]
```

3. **Attach your debug log file**
   - Drag and drop the JSON file into the issue, or
   - Click "Attach files" and select it

### What's in the Debug Logs?

The debug log file contains:

| Section | Description |
|---------|-------------|
| `extensionInfo` | Version, browser, platform info |
| `currentSettings` | Your current extension settings |
| `consoleLogs` | Console output from all extension contexts |
| `storageData` | Current storage state (connection info, etc.) |

> ⚠️ **Privacy Note:** The log file may contain your Room ID and player name. Review the file before sharing if you're concerned about privacy.

---

## 💡 Feature Requests

Have an idea for a new feature? We'd love to hear it!

1. Check if your idea [already exists](https://github.com/DooDesch/TarkovPilotSync/issues?q=is%3Aissue+label%3Aenhancement)
2. If not, [create a new feature request](https://github.com/DooDesch/TarkovPilotSync/issues/new?labels=enhancement)

Please include:
- **What** you want to achieve
- **Why** this feature would be useful
- **How** you envision it working (optional)

---

## 🔧 Troubleshooting

### Common Issues

<details>
<summary><b>Extension doesn't connect</b></summary>

1. Make sure you're on `tarkov-market.com/maps/*`
2. Check if the WebSocket server is reachable
3. Try disconnecting and reconnecting
4. Check the console for error messages (F12 → Console)

</details>

<details>
<summary><b>Players not showing on map</b></summary>

1. Ensure all players are in the same room
2. Check if players are on the same map
3. Verify "Same Map Only" settings in Pins/Quests sections

</details>

<details>
<summary><b>Pins not appearing</b></summary>

1. Check if "Enable Pins" is turned on in settings
2. Verify you're using CTRL+Click to place pins
3. Check "Same Map Only" setting

</details>

<details>
<summary><b>Screenshot Sync not working</b></summary>

1. **Check the status indicator** on the map (bottom left)
   - 🟢 Green = Connected and working
   - 🟠 Orange = Configuration incomplete or folder not connected
   - 🔴 Red = Error occurred

2. **Verify your connection mode**
   - **Desktop App mode:** Verify your Mode is set to "Desktop App" on [tarkov-market.com/pilot](https://tarkov-market.com/pilot)
   - **Hook ID mode:** Verify your Hook-ID from [tarkov-market.com/pilot](https://tarkov-market.com/pilot) (must be a valid UUID format)

3. **Reconnect the folder**
   - Click the status indicator on the map, or
   - Go to extension settings → Screenshot Sync → Select folder

4. **Grant permanent permission**
   - Click "Allow permanently" in settings
   - Select "Allow on every visit" in the browser dialog

5. **Check the screenshot format**
   - Only `.png` files are detected
   - Filename must match Tarkov's format (contains timestamp)

</details>

### Still having issues?

Enable **Debug Mode** in Advanced Settings and reproduce the issue. Then download and share the debug logs in your issue report.

---

## 📜 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ for the Tarkov community

**[DooDesch](https://github.com/DooDesch)**

</div>

