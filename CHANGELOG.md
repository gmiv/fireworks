# Changelog

All notable changes to Fireworks Display Builder will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-11-24

### Initial Release 🎆

#### Features
- **12 Firework Types**: Classic, Peony, Willow, Chrysanthemum, Palm, Crouette, Ring, Heart, Star, Multi-Break, Spiral, Gandalf
- **Color Palette**: 10 vibrant colors with visual swatches
- **Timeline Sequencer**: Track-based show choreography with playback controls
- **Real-time 3D Preview**: Three.js powered particle system (100k particles)
- **8-bit Audio System**: Procedural sound synthesis for launch, explosion, crackle, and magic sounds
- **Save/Load Shows**: JSON export/import functionality
- **Preset Shows**: 4 pre-choreographed demonstrations
  - Opening Burst
  - Crescendo
  - Grand Finale  
  - Gandalf's Display
- **Interactive Canvas**: Click-to-launch fireworks anywhere on screen
- **Timeline Editor**: Add/remove launch events with visual feedback

#### Technical Highlights
- Single-file HTML application (no build tools required)
- 100,000 pre-allocated particle pool with object pooling
- GPU-accelerated rendering with BufferGeometry
- Additive blending for realistic light effects
- 60 FPS smooth animation loop
- Responsive UI with dark theme

#### Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- WebGL required

#### Known Limitations
- Audio requires user gesture (browser security policy)
- Performance scales with particle count
- No timeline zoom functionality yet

---

## Future Roadmap

### v1.1.0 (Planned)
- Mobile touch optimization
- Camera orbit controls
- Additional firework types (strobes, comets)
- Timeline zoom/pan
- Undo/Redo functionality

### v1.2.0 (Planned)
- Video export
- Advanced color patterns
- MIDI controller support
- Multi-track color management

### v2.0.0 (Planned)
- Complete rewrite with modern framework
- Cloud save functionality
- Collaborative editing
- VR/AR support

---

