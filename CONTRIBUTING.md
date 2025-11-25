# Contributing to Fireworks Display Builder

Thank you for your interest in contributing! This project welcomes contributions from developers of all skill levels.

## 🎯 Ways to Contribute

### 1. Report Bugs
- Use GitHub Issues
- Include browser/OS information
- Describe steps to reproduce
- Include screenshots if relevant

### 2. Suggest Features
- Open an issue with "Feature Request" label
- Describe the use case
- Explain expected behavior
- Consider implementation complexity

### 3. Submit Code
- Fork the repository
- Make your changes
- Test thoroughly
- Submit a pull request

## 🔧 Development Setup

No build tools needed! Just:

1. Fork and clone the repo
2. Open `src/fireworks-display-builder.html` in your browser
3. Make changes
4. Refresh to test

## 📝 Code Style

- **Indentation**: 4 spaces
- **Comments**: Use clear section headers with `// ========`
- **Naming**: camelCase for variables, PascalCase for classes
- **Organization**: Keep related code together

## 🧪 Testing Checklist

Before submitting a PR:

- [ ] Test in Chrome, Firefox, and Safari
- [ ] Verify all firework types work
- [ ] Check timeline playback
- [ ] Confirm save/load functionality
- [ ] Test preset shows
- [ ] Verify audio plays correctly
- [ ] Check for console errors
- [ ] Test on different screen sizes

## 🎨 Adding New Firework Types

1. Add entry to `FIREWORK_TYPES` object
2. Include all required parameters:
   - `name`: Display name
   - `particles`: Particle count
   - `speed`: Initial velocity
   - `life`: Duration in seconds
   - `gravity`: Gravitational pull
   - `drag`: Air resistance
   - `size`: Particle size
   - `spread`: Explosion radius
3. Test thoroughly with different colors
4. Update README with new type

## 🔊 Audio Enhancements

When adding new sounds:
- Use Web Audio API only (no external files)
- Keep sounds under 1 second
- Use procedural synthesis for consistency
- Test that AudioContext resumes on user gesture

## 🎨 UI Guidelines

- Maintain dark theme aesthetic
- Use existing color palette
- Keep controls compact and organized
- Ensure responsive behavior
- Test hover states and transitions

## 📚 Documentation

- Update README.md for significant changes
- Add inline comments for complex logic
- Document new parameters/options
- Include usage examples

## 🐛 Bug Fix Process

1. Create issue describing bug
2. Fork and create branch: `fix/issue-number-description`
3. Make minimal changes to fix
4. Test thoroughly
5. Submit PR referencing issue

## ✨ Feature Addition Process

1. Open feature discussion issue first
2. Wait for feedback/approval
3. Fork and create branch: `feature/description`
4. Implement feature
5. Add tests/documentation
6. Submit PR

## 📊 Performance Considerations

- Avoid adding synchronous blocking operations
- Keep particle count reasonable
- Use object pooling for repeated objects
- Profile frame rate during testing
- Optimize BufferGeometry updates

## 🎯 Priority Areas

High-value contributions:

1. **Mobile optimization**
   - Touch controls
   - Performance on mobile GPUs
   - Responsive UI

2. **Export features**
   - Video export
   - Image sequence export
   - Higher quality audio

3. **Advanced effects**
   - Particle trails
   - Secondary explosions
   - Color transitions

4. **Accessibility**
   - Keyboard navigation
   - Screen reader support
   - Reduced motion mode

## ❓ Questions?

- Open a discussion issue
- Tag with "question" label
- Be specific and provide context

## 🙏 Recognition

Contributors will be:
- Listed in README
- Credited in release notes
- Thanked in commit messages

## 📜 Code of Conduct

- Be respectful and constructive
- Welcome newcomers
- Focus on the code, not the person
- Help others learn
- Have fun! 🎆

---

**Happy coding, and thank you for contributing!**
