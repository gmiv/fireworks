# 🎆 Fireworks Display Builder

An interactive real-time fireworks choreography and sequencing tool built with Three.js. Design, preview, and export professional fireworks shows in your browser.

![Fireworks Display Builder Screenshot](screenshot.png)

## ✨ Features

- **12 Firework Types**: Classic, Peony, Willow, Chrysanthemum, Palm, Crouette, Ring, Heart, Star, Multi-Break, Spiral, and Gandalf
- **10 Color Palettes**: Full spectrum of colors for creative expression
- **Timeline Sequencer**: Professional track-based timeline for precise choreography
- **Real-time 3D Preview**: Smooth 60fps rendering with 100,000 particle system
- **8-bit Audio**: Procedurally generated retro-style sound effects
- **Save/Load Shows**: Export and import shows as JSON
- **Preset Shows**: 4 pre-choreographed demonstrations (Opening Burst, Crescendo, Grand Finale, Gandalf's Display)
- **Single File**: No build tools, no dependencies to install - just open and run

## 🚀 Quick Start

1. Download `fireworks-display-builder.html`
2. Open in a modern web browser (Chrome, Firefox, Safari, Edge)
3. Click anywhere on the canvas to launch fireworks
4. Explore the UI controls to build choreographed shows

That's it! No installation, no build process, no server required.

## 🎮 Usage

### Manual Mode
1. Select a firework type from the palette
2. Choose a color
3. Click on the 3D canvas to launch

### Timeline Mode
1. Select firework type and color
2. Scrub the timeline to desired timestamp
3. Click "+" to add a launch event
4. Press Play ▶️ to preview your show
5. Use Loop 🔁 for continuous playback

### Show Management
- **Save**: Download your show as JSON
- **Load**: Import previously saved shows
- **Clear**: Reset timeline to start fresh
- **Presets**: Load demo shows for inspiration

## 🏗️ Architecture

### Technology Stack
- **Three.js r128**: 3D rendering engine
- **Web Audio API**: Real-time sound synthesis
- **Vanilla JavaScript**: No frameworks, minimal dependencies

### Code Structure
```
1. Audio System (8-bit procedural synthesis)
2. Three.js Setup (Scene, camera, renderer)
3. Particle Pool (Pre-allocated 100k particles)
4. Particle Geometry (BufferGeometry for GPU rendering)
5. Firework Types (Physics parameters for each type)
6. Timeline System (Track-based sequencing)
7. Preset Shows (JSON show definitions)
8. UI Controls (Event handlers)
9. Animation Loop (60fps render and physics)
```

### Performance
- **100,000 particles**: Efficiently managed through object pooling
- **60 FPS rendering**: Optimized BufferGeometry updates
- **GPU-accelerated**: THREE.Points with additive blending
- **Dynamic draw range**: Only renders active particles

## 🎨 Customization

### Adding New Firework Types

Edit the `FIREWORK_TYPES` object (~line 820):

```javascript
FIREWORK_TYPES.myCustom = {
    name: 'My Custom',
    particles: 400,      // Number of particles
    speed: 0.3,          // Initial velocity multiplier
    life: 2.0,           // Lifespan in seconds
    gravity: 0.01,       // Downward acceleration
    drag: 0.98,          // Air resistance (0-1)
    size: 3,             // Particle size
    spread: 1,           // Explosion radius multiplier
    trail: true,         // Enable particle trails
    trailDecay: 0.95     // Trail fade rate
};
```

### Adding New Colors

Edit the `colors` array (~line 230):

```javascript
const colors = [
    { name: 'Red', r: 1, g: 0, b: 0 },
    { name: 'Your Color', r: 0.5, g: 0.8, b: 1 },
    // Add more...
];
```

### Creating Preset Shows

Add to the `PRESET_SHOWS` object (~line 1170):

```javascript
PRESET_SHOWS.myShow = {
    name: 'My Show',
    duration: 15,
    tracks: {
        'Track 1': [
            {
                time: 0.5,
                type: 'classic',
                color: { r: 1, g: 0, b: 0 },
                x: 0, y: 10, z: 0
            }
            // Add more launches...
        ]
    }
};
```

## 🔧 Technical Details

### Particle System
- **Pre-allocation**: 100,000 particles created at startup
- **Object Pooling**: Reuses inactive particles for efficiency
- **BufferGeometry**: Direct GPU buffer manipulation
- **Additive Blending**: Creates realistic light bloom

### Physics Simulation
- **Gravity**: Configurable per firework type
- **Drag**: Air resistance simulation
- **Velocity**: 3D vector physics
- **Alpha Fade**: Smooth particle lifecycle

### Audio Synthesis
- **Launch Sound**: Square wave with frequency sweep
- **Explosion**: Quantized noise with decay envelope
- **Crackle**: Multiple frequency pops
- **Magic**: Dual oscillator sweep (for Gandalf)

## 🌐 Browser Compatibility

- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ⚠️ Requires WebGL support
- ⚠️ Best performance on desktop

## 📋 Keyboard Shortcuts

- **Space**: Play/Pause
- **Click Canvas**: Launch firework at click position
- **Timeline Scrub**: Click timeline to jump to time

## 🤝 Contributing

Contributions welcome! Areas for enhancement:

- [ ] More firework types (strobes, comets, shells)
- [ ] Advanced color patterns (gradients, transitions)
- [ ] Camera controls (orbit, zoom, pan)
- [ ] Export to video
- [ ] MIDI controller support
- [ ] Mobile touch optimization
- [ ] Undo/Redo system

## 📄 License

MIT License - see LICENSE file for details

## 🙏 Credits

- **Three.js**: https://threejs.org
- **Geronimo Moralez**: Development and design

## 🐛 Known Issues

- Audio may require user interaction to start (browser security policy)
- Performance scales with particle count - reduce for older hardware
- Timeline zoom not yet implemented

## 📞 Support

Open an issue on GitHub for:
- Bug reports
- Feature requests  
- Questions
- Showcasing your fireworks shows!

---

**Built with ❤️ by Geronimo**

*Made possible by the amazing Three.js community*
