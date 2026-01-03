# ⚡ Quick Start: Multi-Stage Rotation

## 🎯 What is Multi-Stage Rotation?

Multi-Stage Rotation allows you to create **custom scanning sequences** where each stage has its own:
- **Rotation angle** (how far to rotate: -360° to +360°)
- **Tilt angle** (platform tilt: -30° to +30°)

Perfect for complex 3D scanning scenarios!

---

## 🚀 5-Minute Quick Start

### Step 1: Add Your First Stage
1. Scroll to **"Multi-Stage Rotation"** section
2. Click **"Add Stage"** button
3. A new stage appears with default values (360° rotation, 0° tilt)

### Step 2: Configure Stage
Each stage has two inputs:
- **Rotation Angle**: Enter 360 for full rotation, 180 for half, etc.
- **Tilt Angle**: Enter 0 for horizontal, -30 for top view, +30 for bottom view

### Step 3: Add More Stages
Click **"Add Stage"** again to add another stage.

**Example Setup:**
```
Stage 1: Rotation 360° | Tilt 0°    ← Full rotation at horizontal
Stage 2: Rotation 360° | Tilt 10°   ← Full rotation tilted up
Stage 3: Rotation 180° | Tilt -30°  ← Half rotation from top
```

### Step 4: Start Sequence
1. Click **"Start Sequence"**
2. Watch the progress bar
3. Turntable automatically executes each stage in order
4. Returns to zero when complete

---

## 💡 Try the Preset!

Click **"Load Preset"** to see a ready-made configuration:
- Stage 1: 360° rotation at 0° tilt
- Stage 2: 360° rotation at 10° tilt  
- Stage 3: 180° rotation at -30° tilt

This is a great starting point for most objects!

---

## 🎨 Interface Overview

```
┌─────────────────────────────────────────────┐
│  Multi-Stage Rotation                       │
├─────────────────────────────────────────────┤
│                                             │
│  ① [Stage 1]  Rotation: [360°]  Tilt: [0°] │
│  ② [Stage 2]  Rotation: [360°]  Tilt: [10°]│
│  ③ [Stage 3]  Rotation: [180°] Tilt: [-30°]│
│                                             │
│  [+ Add Stage]                              │
│                                             │
│  Progress: ████████░░░░░░░░ 45%           │
│  Current Stage: 2/3  |  Angle: 125°        │
│                                             │
│  [▶ Start] [■ Stop] [Clear] [Load Preset]  │
└─────────────────────────────────────────────┘
```

---

## 🎯 Common Use Cases

### 🏺 Standard 3D Scan
```
Stage 1: 360° at 0°   (horizontal)
Stage 2: 360° at -20° (from above)
Stage 3: 360° at 20°  (from below)
```
**Time:** ~6 min | **Coverage:** Full object

### 💍 Small Object Detail
```
Stage 1: 360° at -30° (top)
Stage 2: 360° at 0°   (middle)
Stage 3: 360° at 30°  (bottom)
```
**Time:** ~6 min | **Coverage:** High detail

### ⚡ Quick Preview
```
Stage 1: 180° at 0°   (front)
Stage 2: 180° at -20° (front-top)
```
**Time:** ~2 min | **Coverage:** Fast preview

---

## 🎛️ Controls Explained

### Add Stage Button
- Adds a new stage to the sequence
- No limit on number of stages
- Each stage can be configured independently

### Stage Controls
- **Number Badge**: Shows stage order (1, 2, 3...)
- **Rotation Input**: -360° to +360°
  - Positive = clockwise
  - Negative = counter-clockwise
- **Tilt Input**: -30° to +30°
  - Negative = tilts toward you (top view)
  - Positive = tilts away (bottom view)
- **Remove Button (X)**: Deletes that stage

### Action Buttons
- **Start Sequence**: Begin executing all stages in order
- **Stop Sequence**: Emergency stop (can restart later)
- **Clear All**: Remove all stages (confirmation required)
- **Load Preset**: Load example 3-stage configuration

### Progress Display
Only visible during execution:
- Current stage number (e.g., "2/5")
- Current rotation angle
- Visual progress bar with percentage

---

## ⚠️ Important Notes

### Limits
- **Rotation**: -360° to +360° per stage
- **Tilt**: -30° to +30° (hardware limit)
- **Stages**: No limit, but 3-7 is optimal

### Behavior
- ✅ Turntable returns to zero rotation between stages
- ✅ Tilt changes before rotation starts
- ✅ Automatically stops at end of sequence
- ✅ Can be stopped at any time with "Stop" button

### Best Practices
- 🎯 Start with 2-3 stages for testing
- 🎯 Use slower speeds for smooth motion
- 🎯 Ensure good lighting at all tilt angles
- 🎯 Test connection before long sequences

---

## 🆚 When to Use Each Mode

### Use **Multi-Stage Rotation** when you need:
- ✅ Different rotation amounts per angle
- ✅ Complex scanning sequences  
- ✅ Full automation from start to finish
- ✅ Custom tilt + rotation combinations

### Use **Auto Rotation Cycle** when you need:
- ✅ Simple 3-position scan
- ✅ Always full 360° rotations
- ✅ Quick setup

### Use **Stepped Rotation** when you need:
- ✅ Precise photo intervals
- ✅ Same angle for all captures
- ✅ Pause between each position

---

## 🎬 Step-by-Step Example

Let's create a basic 3-level scan:

**1. Connect Device**
```
Click "Connect Device" → Select turntable → Wait for "Connected"
```

**2. Add Stages**
```
Click "Add Stage" (3 times)
```

**3. Configure Stage 1**
```
Stage 1: Rotation: 360 | Tilt: 0
(Leave as default - full rotation at horizontal)
```

**4. Configure Stage 2**
```
Stage 2: Rotation: 360 | Tilt: 10
(Full rotation with slight upward tilt)
```

**5. Configure Stage 3**
```
Stage 3: Rotation: 180 | Tilt: -30
(Half rotation from top view - saves time!)
```

**6. Start**
```
Click "Start Sequence"
Watch progress bar
Wait for completion (~5 minutes)
```

**Done!** Your turntable just performed a complete multi-angle scan!

---

## 🐛 Quick Troubleshooting

**Q: Stage won't start**  
A: Check Bluetooth connection (green indicator top-right)

**Q: Rotation angle not accurate**  
A: Reduce speed in "Speed Control" section

**Q: Can't add stages**  
A: Refresh page if button not responding

**Q: Progress bar stuck**  
A: Click "Stop" and restart sequence

**Q: Tilt not reaching angle**  
A: Check if within -30° to +30° limits

---

## 📚 Learn More

- **Full Documentation**: See [README.md](README.md)
- **More Examples**: See [EXAMPLES.md](EXAMPLES.md)
- **Troubleshooting**: See README Troubleshooting section

---

## 🎯 Next Steps

1. ✅ Try the preset configuration
2. ✅ Modify one value at a time
3. ✅ Experiment with different angles
4. ✅ Create your own custom sequences
5. ✅ Share your configurations with the community!

---

<div align="center">

**Ready to create your first multi-stage scan?**

[Open DAT.html](DAT.html) and scroll to "Multi-Stage Rotation"!

</div>

