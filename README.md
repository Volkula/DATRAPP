# 🔄 Revopoint DAT Controller

<div align="center">

![Version](https://img.shields.io/badge/version-2.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Web Bluetooth](https://img.shields.io/badge/Web%20Bluetooth-API-purple.svg)

**Advanced Web Interface for Revopoint Dual Axis Turntable Control**

[Features](#-features) • [Quick Start](#-quick-start) • [Usage](#-usage) • [API](#-api-reference) • [Troubleshooting](#-troubleshooting)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Requirements](#-requirements)
- [Quick Start](#-quick-start)
- [Usage Guide](#-usage-guide)
- [Technical Documentation](#-technical-documentation)
- [API Reference](#-api-reference)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

**Revopoint DAT Controller** is a modern, feature-rich web application for controlling the Revopoint Dual Axis Turntable via Web Bluetooth API. This application provides intuitive controls for 3D scanning, photography, and product visualization workflows.

### What is a Dual Axis Turntable?

A dual axis turntable is a motorized platform with two independent rotation axes:
- **Rotation Axis (CT)**: 360° horizontal spinning
- **Tilt Axis (CR)**: Vertical tilting (typically -30° to +30°)

This allows for comprehensive 3D capture from multiple angles automatically.

---

## ✨ Features

### 🎨 Modern User Interface
- **Beautiful gradient design** with smooth animations
- **Responsive layout** - works on desktop, tablet, and mobile
- **Real-time connection status** indicator with click-to-connect/disconnect
- **Interactive tooltips** for better user guidance
- **Dark theme** optimized for extended use
- **Quick connect badge** - connect/disconnect with one click from anywhere

### 🎮 Control Modes

#### 1. **Manual Rotation Control**
- Precise angle input for rotation
- Quick preset buttons (360° left/right)
- Continuous rotation mode (infinite rotation)
- Return to zero position
- Emergency stop function

#### 2. **Manual Tilt Control**
- Adjustable tilt increments
- Quick preset angles (-30°, -20°, -10°, +10°, +20°, +30°)
- Zero tilt position
- Independent tilt stop

#### 3. **Speed Control**
- **Rotation speed**: 35.64 - 131 (adjustable via slider)
- **Tilt speed**: 9 - 35 (adjustable via slider)
- Real-time speed adjustment
- Visual feedback with smooth sliders

#### 4. **Automatic Rotation Cycle**
- Program up to 3 tilt positions
- Automatic rotation through programmed positions
- Full 360° rotation at each position
- Perfect for multi-angle 3D scanning

#### 5. **Stepped Rotation Mode**
- Divide 360° into any number of steps (e.g., 36 steps = 10° each)
- Configurable pause time between steps
- Pause/resume functionality
- Manual step forward/backward
- Ideal for photogrammetry workflows

#### 6. **Multi-Stage Rotation (NEW!)**
- Create custom sequences with multiple stages
- Configure rotation angle and tilt for each stage independently
- Add/remove stages dynamically
- Real-time progress tracking with visual progress bar
- Save and load presets
- Perfect for complex 3D scanning scenarios
- Example: 360° at 0°, 360° at 10°, 180° at -30°

#### 7. **Keyboard Shortcuts**
- `W` - Tilt up (+1°)
- `S` - Tilt down (-1°)
- `A` - Rotate left (+1°)
- `D` - Rotate right (-1°)
- Quick control without mouse interaction

---

## 📦 Requirements

### Hardware
- Revopoint Dual Axis Turntable (DAT)
- Computer/device with Bluetooth capability
- Bluetooth 4.0 or higher (BLE support)

### Software
- Modern web browser with Web Bluetooth API support:
  - ✅ Chrome 56+ (recommended)
  - ✅ Edge 79+
  - ✅ Opera 43+
  - ❌ Firefox (Web Bluetooth not supported by default)
  - ❌ Safari (Web Bluetooth not supported)

### Operating Systems
- ✅ Windows 10/11
- ✅ macOS (Chrome/Edge only)
- ✅ Linux (with BlueZ 5.41+)
- ✅ Android 6.0+
- ⚠️ iOS (limited support)

---

## 🚀 Quick Start

### Step 1: Open the Application

Simply open the `DAT.html` file in a compatible browser:

```bash
# Option 1: Direct file open
# Right-click DAT.html → Open with → Chrome

# Option 2: Local server (recommended)
python -m http.server 8000
# Then navigate to: http://localhost:8000/DAT.html

# Option 3: Using Node.js
npx serve
```

### Step 2: Enable Bluetooth

Ensure Bluetooth is enabled on your device:
- **Windows**: Settings → Bluetooth & devices → Turn on Bluetooth
- **macOS**: System Preferences → Bluetooth → Turn Bluetooth On
- **Linux**: `sudo systemctl start bluetooth`

### Step 3: Power On Turntable

1. Turn on your Revopoint DAT turntable
2. Wait for the device to enter pairing mode (LED indicator)
3. Device should be discoverable as "Revopoint" or similar

### Step 4: Connect

**Option 1: Quick Connect (Status Badge)**
1. Click the **status badge** in the top-right corner (shows "Disconnected")
2. Select your turntable from the Bluetooth device list
3. Click **"Pair"**
4. Status badge will turn green and show "Connected"

**Option 2: Connection Card**
1. Click the **"Connect Device"** button in the Connection section
2. Select your turntable from the Bluetooth device list
3. Click **"Pair"**
4. Connection status will show "Connected" in green

**💡 Tip:** You can click the status badge anytime to connect/disconnect!

### Step 5: Start Controlling

You're ready! Try basic controls:
- Adjust speed sliders
- Click rotation arrows
- Test keyboard shortcuts (W/A/S/D)

---

## 📖 Usage Guide

### Basic Rotation

1. **Set rotation speed** using the top slider (35.64 - 131)
2. **Enter angle** in the rotation input field (default: 10°)
3. **Click arrows** to rotate left (←) or right (→)
4. **Click "Zero"** to return to starting position

### Tilt Control

1. **Set tilt speed** using the second slider (9 - 35)
2. **Enter tilt amount** in the input field (default: 15°)
3. **Click +/-** buttons to tilt up or down
4. **Use preset buttons** for quick angles

### Automatic 3D Scanning Workflow

Perfect for capturing objects from multiple angles:

1. **Go to "Auto Rotation Cycle" section**
2. **Set three tilt positions**:
   - Position 1: `0°` (horizontal)
   - Position 2: `-30°` (looking down)
   - Position 3: `15°` (looking up)
3. **Click "Start Cycle"**
4. The turntable will:
   - Move to position 1 → Rotate 360° → Capture
   - Move to position 2 → Rotate 360° → Capture
   - Move to position 3 → Rotate 360° → Capture
   - Return to zero

### Photogrammetry Workflow

For taking photos at regular intervals:

1. **Go to "Stepped Rotation" section**
2. **Set steps per 360°**: 
   - 36 steps = 10° per photo
   - 72 steps = 5° per photo
   - 24 steps = 15° per photo
3. **Set pause time**: 2500ms = 2.5 seconds between positions
4. **Click "Start"**
5. Camera trigger can be manual or automatic during pauses
6. Use **"Pause"** to adjust camera/lighting between shots

### Multi-Stage Rotation Workflow (Advanced)

Create complex scanning sequences with full control:

1. **Go to "Multi-Stage Rotation" section**
2. **Click "Add Stage"** for each scanning position
3. **Configure each stage**:
   - **Rotation Angle**: -360° to 360° (negative = left, positive = right)
   - **Tilt Angle**: -30° to 30° (platform tilt position)
4. **Example configurations**:

   **Basic 3-Level Scan:**
   - Stage 1: Rotation 360°, Tilt 0° (horizontal view)
   - Stage 2: Rotation 360°, Tilt 10° (slight angle)
   - Stage 3: Rotation 180°, Tilt -30° (top-down view)

   **Detailed Object Scan:**
   - Stage 1: Rotation 360°, Tilt -30° (from above)
   - Stage 2: Rotation 360°, Tilt -15°
   - Stage 3: Rotation 360°, Tilt 0° (horizontal)
   - Stage 4: Rotation 360°, Tilt 15°
   - Stage 5: Rotation 360°, Tilt 30° (from below)

5. **Click "Start Sequence"** to begin
6. **Monitor progress** in real-time with the progress bar
7. **Use presets** for quick setup with "Load Preset"

**Tips:**
- ✅ Test with smaller rotation angles first (90°-180°)
- ✅ Use "Load Preset" to see example configurations
- ✅ Each stage automatically returns to zero before next stage
- ✅ Click "Stop Sequence" at any time to halt execution
- ✅ Save complex sequences by noting down the values

### Tips & Best Practices

✅ **DO:**
- Start with slower speeds for precision work
- Use "Zero" position as your reference point
- Test your automation with "Stop" readily available
- Allow proper settling time in stepped mode (2-3 seconds)

❌ **DON'T:**
- Don't exceed tilt limits (-30° to +30°)
- Don't run multiple automation modes simultaneously
- Don't disconnect while turntable is moving
- Don't change speeds during active rotation (pause first)

---

## 🔧 Technical Documentation

### Architecture

```
┌─────────────────────────────────────────┐
│         Web Browser (Client)            │
│  ┌───────────────────────────────────┐  │
│  │     DAT.html (UI)                 │  │
│  │  - HTML5 Interface                │  │
│  │  - CSS3 Styling + Animations      │  │
│  │  - Vanilla JavaScript Logic       │  │
│  └───────────┬───────────────────────┘  │
│              │ Web Bluetooth API        │
│  ┌───────────▼───────────────────────┐  │
│  │   Browser Bluetooth Stack         │  │
│  └───────────┬───────────────────────┘  │
└──────────────┼─────────────────────────┘
               │ BLE Connection
     ┌─────────▼──────────┐
     │  Revopoint DAT     │
     │  ┌──────────────┐  │
     │  │ Service:     │  │
     │  │ 0xFFE0       │  │
     │  │ ┌──────────┐ │  │
     │  │ │ Char:    │ │  │
     │  │ │ 0xFFE1   │ │  │
     │  │ │ (R/W)    │ │  │
     │  │ └──────────┘ │  │
     │  └──────────────┘  │
     │                    │
     │  Motors & Control  │
     └────────────────────┘
```

### Bluetooth Protocol

#### Service & Characteristic
- **Primary Service UUID**: `0xFFE0`
- **Characteristic UUID**: `0xFFE1` (Read/Write)
- **Encoding**: UTF-8 text commands

#### Command Format
All commands follow the pattern: `+PREFIX,COMMAND=VALUE;`

### Multi-Stage Rotation Interface

The Multi-Stage Rotation feature provides a powerful interface for creating complex scanning sequences:

**UI Components:**
1. **Stage List** - Visual list of all configured stages with numbering
2. **Stage Controls** - Each stage has:
   - Rotation angle input (-360° to +360°)
   - Tilt angle input (-30° to +30°)
   - Remove button (delete individual stage)
3. **Action Buttons**:
   - **Add Stage** - Add new stage to sequence
   - **Start Sequence** - Execute all stages in order
   - **Stop Sequence** - Emergency stop during execution
   - **Clear All** - Remove all stages
   - **Load Preset** - Load example configuration
4. **Progress Display** - Shows:
   - Current stage number
   - Current rotation angle
   - Visual progress bar with percentage

**Workflow:**
```
User adds stages → Configure angles → Start sequence
  ↓                    ↓                    ↓
Visual list      Input validation    Real-time feedback
  ↓                    ↓                    ↓
Empty state      Min/max limits      Progress tracking
                                           ↓
                                    Auto-return to zero
```

### Command Reference

#### Rotation (CT) Commands

| Command | Description | Example |
|---------|-------------|---------|
| `+CT,TURNSPEED=X;` | Set rotation speed | `+CT,TURNSPEED=50;` |
| `+CT,TURNANGLE=X;` | Rotate by X degrees | `+CT,TURNANGLE=90;` |
| `+CT,TURNCONTINUE=X;` | Continuous rotation | `+CT,TURNCONTINUE=1;` (1=right, -1=left) |
| `+CT,TOZERO;` | Return to zero | `+CT,TOZERO;` |
| `+CT,STOP;` | Stop rotation | `+CT,STOP;` |

#### Tilt (CR) Commands

| Command | Description | Example |
|---------|-------------|---------|
| `+CR,TILTSPEED=X;` | Set tilt speed | `+CR,TILTSPEED=15;` |
| `+CR,TILTVALUE=X;` | Tilt by X degrees | `+CR,TILTVALUE=-20;` |
| `+CR,TOZERO;` | Return to zero tilt | `+CR,TOZERO;` |
| `+CR,STOP;` | Stop tilt | `+CR,STOP;` |

#### Query Commands

| Command | Description | Response |
|---------|-------------|----------|
| `+QT,CHANGEANGLE;` | Get current angle | `+DATA=90;` |

### Code Structure

```javascript
// Core Functions
async function connect()              // Establish Bluetooth connection
async function bluetoothSend(cmd)     // Send command and receive response
async function set_rotation_speed()   // Update rotation speed
async function set_tilt_speed()       // Update tilt speed
async function getvalue(a, b)         // Poll current angle during automation
function sleep(ms)                    // Async delay utility

// Event Handlers
ct_forward/backward                   // Manual rotation controls
cr_forward/backward                   // Manual tilt controls
a_rot_start/stop                      // Automatic cycle controls
sp_start/pause/stop                   // Stepped rotation controls
sp_step_forward/back                  // Manual step controls
keydown event listener                // Keyboard shortcuts
```

### State Management

```javascript
// Connection State
server: false | BluetoothRemoteGATTServer

// Runtime Flags
button_stop_pressed: boolean          // Stop automation flag
pause_read_result: boolean            // Pause angle reading
getvalue_running: boolean             // Automation in progress
rws_status: boolean                   // Stepped rotation active
rws_pause: boolean                    // Stepped rotation paused

// Position Tracking
tiltvalue: number                     // Current keyboard tilt value
sp_current_step: number               // Current step in sequence
```

---

## 🔌 API Reference

### JavaScript API

#### Connect to Device

```javascript
async function connect()
```

**Returns**: `Promise<BluetoothRemoteGATTServer>`

**Usage**:
```javascript
const server = await connect();
if (server) {
    console.log("Connected successfully!");
}
```

#### Send Bluetooth Command

```javascript
async function bluetoothSend(cmd: string)
```

**Parameters**:
- `cmd` (string): Command string in protocol format

**Returns**: `Promise<string>` - Response from device

**Usage**:
```javascript
// Rotate 45 degrees
const response = await bluetoothSend('+CT,TURNANGLE=45;');

// Set tilt to -20 degrees
await bluetoothSend('+CR,TILTVALUE=-20;');

// Query current position
const angle = await bluetoothSend('+QT,CHANGEANGLE;');
// Response: "+DATA=123;"
```

#### Speed Control

```javascript
async function set_rotation_speed(event)
async function set_tilt_speed(event)
```

**Parameters**:
- `event`: Input change event with `.value` property

**Usage**:
```html
<input type="range" onchange="set_rotation_speed(this)" />
```

---

## 🐛 Troubleshooting

### Connection Issues

#### Problem: "Connect Device" button does nothing

**Solutions**:
1. ✅ Ensure you're using a compatible browser (Chrome/Edge)
2. ✅ Check browser console for errors (F12)
3. ✅ Verify Bluetooth is enabled on your device
4. ✅ Try HTTPS connection (Web Bluetooth requires secure context)
5. ✅ Reload the page and try again

#### Problem: Device not appearing in pairing list

**Solutions**:
1. ✅ Verify turntable is powered on
2. ✅ Check if device is already connected to another device
3. ✅ Move closer to turntable (within 10 meters)
4. ✅ Restart turntable
5. ✅ Clear browser Bluetooth cache (Chrome settings → Privacy → Site data)

#### Problem: "GATT Server Disconnected" error

**Solutions**:
1. ✅ Check battery level of turntable
2. ✅ Reduce distance between device and turntable
3. ✅ Minimize interference (WiFi routers, other BT devices)
4. ✅ Reconnect using "Connect Device" button

### Control Issues

#### Problem: Commands not executing

**Solutions**:
1. ✅ Check connection status indicator (top-right)
2. ✅ Verify command syntax in browser console
3. ✅ Ensure previous command completed
4. ✅ Click "Stop" then retry command

#### Problem: Turntable moving erratically

**Solutions**:
1. ✅ Lower rotation/tilt speed
2. ✅ Check for mechanical obstructions
3. ✅ Calibrate using "Zero" buttons
4. ✅ Restart turntable and reconnect

#### Problem: Stepped rotation not stopping correctly

**Solutions**:
1. ✅ Click "Stop" button (not browser stop)
2. ✅ Wait for current step to complete
3. ✅ Manually send stop command: `+CT,STOP;`
4. ✅ Reload page if unresponsive

### Browser Compatibility

#### Problem: Web Bluetooth not available

**Check browser compatibility**:
```javascript
// Open browser console and run:
if (navigator.bluetooth) {
    console.log("✅ Web Bluetooth supported");
} else {
    console.log("❌ Web Bluetooth not supported");
}
```

**Solutions**:
1. ✅ Use Chrome/Edge browser
2. ✅ Enable experimental features (chrome://flags → #enable-web-bluetooth)
3. ✅ Update browser to latest version
4. ✅ Use HTTPS or localhost

### Performance Issues

#### Problem: Slow response or lag

**Solutions**:
1. ✅ Close unnecessary browser tabs
2. ✅ Reduce animation complexity (if modified)
3. ✅ Check Bluetooth signal strength
4. ✅ Disable browser extensions
5. ✅ Try different USB Bluetooth adapter (desktop)

---

## 🎨 Customization

### Modifying Colors

Edit CSS variables in the `:root` selector:

```css
:root {
    --primary-color: #667eea;      /* Main accent color */
    --secondary-color: #764ba2;    /* Secondary accent */
    --accent-color: #f093fb;       /* Highlight color */
    --bg-dark: #0f0f23;           /* Background */
    --bg-card: #1a1a2e;           /* Card background */
}
```

### Adding Custom Commands

```javascript
// Add to script section
async function customCommand() {
    await bluetoothSend('+CT,TURNANGLE=180;');
    await sleep(5000);
    await bluetoothSend('+CR,TILTVALUE=15;');
}

// Add button in HTML
<button onclick="customCommand()">
    <i class="fas fa-magic"></i> Custom Move
</button>
```

### Keyboard Shortcuts

Add new shortcuts in the keyboard event listener:

```javascript
document.addEventListener("keydown", (e) => {
    if (e.target.tagName === 'INPUT') return;
    
    switch (e.key.toLowerCase()) {
        case "r":  // Add 'R' for reset
            bluetoothSend('+CT,TOZERO;');
            bluetoothSend('+CR,TOZERO;');
            break;
        // ... existing cases
    }
});
```

---

## 📊 Advanced Usage

### Integration with 3D Scanning Software

Many 3D scanning applications can be synchronized with the turntable:

1. **Use Stepped Rotation Mode** for simple scans
2. **Use Multi-Stage Rotation** for complex sequences
3. **Set appropriate pause time** for scan completion
4. **Configure software to trigger on:**
   - Timer (match pause duration)
   - Keyboard shortcut
   - Network trigger

### Photogrammetry Pipeline

Example workflow for high-quality captures:

```javascript
// Configuration for 36 photos per rotation
Steps: 36 (10° per photo)
Pause: 3000ms (3 seconds)

// Tilt sequence for 3-level capture
Tilt 1: 0°   (horizontal)
Tilt 2: -25° (above)
Tilt 3: 15°  (below)

// Total photos: 36 × 3 = 108 images
```

### Multi-Stage Scanning Pipeline

Example configurations for different object types:

**Small Object (Jewelry, Coins):**
```javascript
// 5-stage high-detail scan
Stage 1: Rotation 360°, Tilt -30° (top)
Stage 2: Rotation 360°, Tilt -15° 
Stage 3: Rotation 360°, Tilt 0°   (middle)
Stage 4: Rotation 360°, Tilt 15°
Stage 5: Rotation 360°, Tilt 30°  (bottom)

// Total coverage: 5 full rotations from different angles
```

**Medium Object (Figurines, Bottles):**
```javascript
// 3-stage balanced scan
Stage 1: Rotation 360°, Tilt 0°   (horizontal)
Stage 2: Rotation 360°, Tilt -20° (top angle)
Stage 3: Rotation 180°, Tilt 20°  (bottom angle, partial)

// Total: 2.5 rotations with varied perspectives
```

**Large Object (Sculptures, Furniture):**
```javascript
// 4-stage comprehensive scan
Stage 1: Rotation 180°, Tilt -30° (top-front)
Stage 2: Rotation 180°, Tilt -30° (reset + top-back)
Stage 3: Rotation 360°, Tilt 0°   (full horizontal)
Stage 4: Rotation 180°, Tilt 25°  (bottom angle)

// Covers all major angles without redundancy
```

### Remote Control via JavaScript Console

For advanced users, control directly via browser console:

```javascript
// Quick 360 panorama
async function quickPano() {
    await bluetoothSend('+CT,TURNSPEED=60;');
    for (let i = 0; i < 12; i++) {
        await bluetoothSend('+CT,TURNANGLE=30;');
        await sleep(3000);
        console.log(`Photo ${i + 1}/12 - Angle: ${i * 30}°`);
    }
}

quickPano();
```

---

## 🔒 Security & Privacy

### Data Handling
- ✅ **No data collection**: Application runs entirely client-side
- ✅ **No external requests**: No analytics or tracking
- ✅ **Local storage only**: Settings saved in browser localStorage
- ✅ **Bluetooth only**: No internet connection required

### Permissions Required
- **Bluetooth**: For device communication (user must approve)
- **No camera/microphone**: Not required or requested
- **No location**: Not required or requested

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Reporting Bugs
1. Check existing issues first
2. Provide browser version and OS
3. Include console error messages
4. Describe steps to reproduce

### Suggesting Features
- Open an issue with `[Feature Request]` tag
- Describe use case and benefits
- Provide mockups if applicable

### Code Contributions
1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

### Development Setup

```bash
# Clone repository
git clone https://github.com/yourusername/revopoint-dat-controller.git

# No build process needed - pure HTML/CSS/JS!
# Just open DAT.html in browser

# For testing, use local server:
python -m http.server 8000
# or
npx serve
```

---

## 📝 License

MIT License - see LICENSE file for details

---

## 🙏 Acknowledgments

- **Revopoint** for the DAT hardware
- **Web Bluetooth Community** for documentation and examples
- **Font Awesome** for beautiful icons
- All contributors and users providing feedback

---

## 📞 Support

### Documentation
- **GitHub Issues**: [Report bugs or request features]
- **Wiki**: [Additional tutorials and guides]

### Community
- **Discord**: [Join our community]
- **Forum**: [Revopoint official forum]

### Contact
- **Email**: support@yourproject.com
- **Twitter**: @yourproject

---

## 📈 Changelog

### Version 2.2 (Current)
- ✨ **NEW: Click-to-connect status badge** - connect/disconnect with one click
- ✨ Improved disconnect handling - safely stops all operations
- ✨ Interactive status indicator with hover effects
- ✨ Context-aware tooltips on status badge
- 🐛 Fixed GATT operation conflicts with mutex protection
- 🐛 Fixed error handling for null responses
- 🐛 Added delays between Bluetooth commands for stability
- 🐛 Improved error recovery in all automation modes

### Version 2.1
- ✨ **NEW: Multi-Stage Rotation mode** with custom sequences
- ✨ Add/remove stages dynamically with visual interface
- ✨ Real-time progress tracking with animated progress bar
- ✨ Load preset configurations for quick setup
- ✨ Independent rotation and tilt control per stage
- ✨ Visual feedback during multi-stage execution
- 📚 Updated documentation with multi-stage examples
- 🎨 Enhanced UI animations for stage management

### Version 2.0
- ✨ Complete UI redesign with modern gradient theme
- ✨ Added smooth animations and transitions
- ✨ Real-time connection status indicator
- ✨ Interactive tooltips on all buttons
- ✨ Improved keyboard controls
- ✨ Better error handling and feedback
- ✨ Mobile-responsive design
- 🐛 Fixed tilt calculation spacing in keyboard commands
- 🐛 Improved connection stability
- 📚 Comprehensive documentation

### Version 1.0
- ⚡ Initial release
- ⚡ Basic rotation and tilt control
- ⚡ Automatic cycle mode
- ⚡ Stepped rotation mode
- ⚡ Keyboard shortcuts

---

<div align="center">

**Made with ❤️ for the 3D Scanning Community**

[⬆ Back to Top](#-revopoint-dat-controller)

</div>

