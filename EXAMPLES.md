# 🎯 Multi-Stage Rotation Examples

This document provides ready-to-use configurations for the Multi-Stage Rotation feature.

## 🚀 Try It Live!

**[→ Launch Live Demo ←](https://htmlpreview.github.io/?https://github.com/Volkula/DATRAPP/blob/main/DAT.html)**

*Test these examples directly in your browser - no installation needed!*

---

## 📦 Quick Start Examples

### Example 1: Basic 3-Level Scan
**Best for:** General 3D scanning, medium-sized objects

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 360° | 0° | Full horizontal scan |
| 2 | 360° | 10° | Slight upward angle |
| 3 | 180° | -30° | Top-down view (half rotation) |

**Total captures:** ~2.5 full rotations  
**Time:** ~5-7 minutes (depending on speed)

---

### Example 2: High-Detail Small Object
**Best for:** Jewelry, coins, small collectibles

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 360° | -30° | Top view |
| 2 | 360° | -15° | Upper angle |
| 3 | 360° | 0° | Horizontal |
| 4 | 360° | 15° | Lower angle |
| 5 | 360° | 30° | Bottom view |

**Total captures:** 5 full rotations  
**Time:** ~8-12 minutes  
**Coverage:** Complete 360° coverage from all vertical angles

---

### Example 3: Fast Preview Scan
**Best for:** Quick preview, testing lighting/setup

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 180° | 0° | Front hemisphere |
| 2 | 180° | -20° | Top angle |

**Total captures:** 1 full rotation (2 × 180°)  
**Time:** ~2-3 minutes  
**Use case:** Quick test before full scan

---

### Example 4: Tall Object Scan
**Best for:** Bottles, vases, tall sculptures

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 360° | -25° | Top portion |
| 2 | 360° | 0° | Middle portion |
| 3 | 360° | 25° | Bottom portion |

**Total captures:** 3 full rotations  
**Time:** ~6-9 minutes  
**Coverage:** Vertical coverage optimized for tall objects

---

### Example 5: Flat Object (Coins, Medals)
**Best for:** Coins, medals, flat items

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 360° | -30° | Top face capture |
| 2 | 360° | 0° | Edge capture |
| 3 | 180° | 30° | Bottom face partial |

**Total captures:** 2.5 rotations  
**Time:** ~4-6 minutes  
**Note:** Focuses on top surface and edges

---

### Example 6: Large Sculpture
**Best for:** Busts, large figurines, art pieces

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 90° | -30° | Front-top-right |
| 2 | 90° | -30° | Front-top-left |
| 3 | 90° | -30° | Back-top-right |
| 4 | 90° | -30° | Back-top-left |
| 5 | 360° | 0° | Full horizontal |
| 6 | 180° | 20° | Bottom angles |

**Total captures:** 3.5 rotations  
**Time:** ~8-10 minutes  
**Coverage:** Systematic coverage of all faces

---

### Example 7: Photogrammetry Optimized
**Best for:** High-quality photogrammetry reconstruction

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 360° | -30° | Upper ring |
| 2 | 360° | -20° | Upper-mid ring |
| 3 | 360° | -10° | Mid-upper ring |
| 4 | 360° | 0° | Equator ring |
| 5 | 360° | 10° | Mid-lower ring |
| 6 | 360° | 20° | Lower-mid ring |
| 7 | 360° | 30° | Lower ring |

**Total captures:** 7 full rotations  
**Time:** ~15-20 minutes  
**Coverage:** Maximum detail with overlapping coverage  
**Best with:** 36-72 photos per rotation (stepped mode)

---

### Example 8: Asymmetric Object
**Best for:** Objects interesting from one side only

| Stage | Rotation | Tilt | Description |
|-------|----------|------|-------------|
| 1 | 180° | -20° | Front upper |
| 2 | 180° | 0° | Front middle |
| 3 | 180° | 20° | Front lower |
| 4 | 90° | 0° | Side detail |

**Total captures:** 2.25 rotations  
**Time:** ~4-5 minutes  
**Note:** Saves time by focusing on interesting angles

---

## 🎨 Usage Tips

### Speed Settings
- **Fast scan (60-80 speed):** Quick preview, less detail
- **Medium scan (40-60 speed):** Balanced quality/time
- **Slow scan (35-40 speed):** Maximum quality, smooth video

### Combining with Stepped Mode
For photogrammetry, use Multi-Stage for tilt sequences, then:
1. Configure stepped rotation (e.g., 36 steps)
2. Manually trigger each stage
3. Camera captures at each step

### Safety Limits
- **Rotation:** -360° to +360° per stage
- **Tilt:** -30° to +30° (device physical limit)
- **Stages:** Unlimited, but 3-7 stages optimal

### Performance
- Each stage adds ~1-3 minutes
- Transitions between stages: ~2-3 seconds
- Plan for 1.5× estimated time (includes settling)

---

## 🔧 Custom Configurations

### Creating Your Own Sequence

**Step 1: Define Your Goal**
- Full coverage? → Use 5-7 stages with varied tilts
- Quick preview? → Use 2-3 stages
- Specific detail? → Focus rotations on that area

**Step 2: Calculate Rotations**
```
Full sphere coverage = 3-5 full rotations minimum
Half sphere (objects with flat base) = 2-3 rotations
Quarter coverage (relief/flat) = 1-2 rotations
```

**Step 3: Distribute Tilt Angles**
```
Even distribution for spherical objects:
  -30°, -15°, 0°, 15°, 30°

Weighted for tall objects:
  -25°, -10°, 0°, 10°, 25°

Top-heavy for flat objects:
  -30°, -20°, -10°, 0°
```

**Step 4: Optimize Rotation Angles**
- Use 360° for complete rings
- Use 180° for partial coverage (saves time)
- Use 90° for specific quadrants only

---

## 🎬 Workflow Integration

### With 3D Scanning Software
```
1. Setup Multi-Stage sequence
2. Start sequence in DAT Controller
3. Software auto-captures at each position
4. Post-process in scanning software
```

### With Manual Photography
```
1. Setup Multi-Stage sequence
2. Set appropriate pause times
3. Manually trigger camera at each position
4. Use stepped rotation for precise intervals
```

### With Video Capture
```
1. Setup Multi-Stage with slow speed
2. Start video recording
3. Run sequence (continuous smooth motion)
4. Extract frames in post-processing
```

---

## 💡 Pro Tips

1. **Test First:** Always run a quick 2-stage test before full sequence
2. **Lighting:** Check shadows at each tilt angle before starting
3. **Background:** Ensure background visible at all angles
4. **Calibration:** Use "Zero" before each sequence for consistency
5. **Save Settings:** Note successful configurations for reuse
6. **Monitor Progress:** Watch first few stages to verify expected behavior
7. **Battery:** Ensure device fully charged for long sequences
8. **Bluetooth Range:** Stay within 5 meters for stable connection

---

## 🐛 Troubleshooting

**Stage skips angles:**
- Reduce rotation speed
- Increase settling time (add pauses)
- Check mechanical obstructions

**Tilt not reaching position:**
- Verify tilt limits (-30° to +30°)
- Check device calibration
- Reduce tilt speed for accuracy

**Sequence stops mid-execution:**
- Check Bluetooth connection
- Verify device battery
- Reduce sequence length (split into parts)

---

## 📝 Template

Copy and fill this template for your custom configurations:

```
Configuration Name: _________________
Object Type: _________________
Estimated Time: _________________

Stage 1: Rotation ___° | Tilt ___° | Purpose: _________________
Stage 2: Rotation ___° | Tilt ___° | Purpose: _________________
Stage 3: Rotation ___° | Tilt ___° | Purpose: _________________
Stage 4: Rotation ___° | Tilt ___° | Purpose: _________________
Stage 5: Rotation ___° | Tilt ___° | Purpose: _________________

Notes: _________________________________________________
_______________________________________________________
```

---

**Need more help?** Check the main [README.md](README.md) for complete documentation!

---

<div align="center">

Made with ❤️ for the 3D Scanning Community

*Based on the [original controller by eXplOiD1](https://github.com/eXplOiD1/Revopoint-Dual-Axis-Turntable-webbased-Controller/)*

</div>

