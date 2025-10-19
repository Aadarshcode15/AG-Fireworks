# 🎆 Spectacular Fireworks Display

An interactive, browser-based fireworks animation featuring realistic particle physics, multiple firework types, and procedurally generated sound effects using HTML5 Canvas and Web Audio API.

![Fireworks Display](https://img.shields.io/badge/HTML5-Canvas-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-Animations-1572B6?style=flat&logo=css3&logoColor=white)

## ✨ Features

### Visual Effects
- **5 Unique Firework Types**:
  - **Burst**: Classic circular explosion with colorful particles
  - **Ring**: Perfect ring-shaped expansion
  - **Willow**: Cascading waterfall effect
  - **Mega**: Double-layered explosion with delayed secondary burst
  - **Crackling**: Random scatter pattern with multiple pops

- **Realistic Physics Engine**:
  - Gravity simulation
  - Velocity and friction calculations
  - Alpha decay for natural fading
  - Particle trail effects

- **Dynamic Particle System**:
  - Star-shaped and circular particles
  - Glowing effects with shadow blur
  - Color variations and brightness controls
  - Trail persistence for motion blur

### Audio Features
- **4-Layer Realistic Explosion Sounds**:
  - Deep bass boom (low-frequency rumble)
  - White noise burst (main explosion)
  - Mid-frequency punch (sharp crack)
  - High-frequency sparkle (sizzling effect)

- **Additional Sound Effects**:
  - Realistic whistle sounds for rocket launches
  - Scattered crackle effects with band-pass filtering
  - Pop sounds for small explosions
  - Intensity-scaled audio based on firework size

- **Procedurally Generated**: All sounds created with Web Audio API (no external files needed)

### Interactive Controls
- **Click to Launch**: Click anywhere on the canvas to launch fireworks toward that position
- **Auto Launch Mode**: Toggle automatic random firework launches
- **Sound Toggle**: Enable/disable all sound effects
- **Clear Canvas**: Reset the display and clear all particles

## 🚀 Getting Started

### Prerequisites
- Modern web browser with HTML5 Canvas support
- JavaScript enabled
- Web Audio API support (all modern browsers)

### Installation

1. **Download the file**:
Clone or download the HTML file
wget https://yourdomain.com/fireworks.html

2. **Open in browser**:
- Simply double-click the `fireworks.html` file, or
- Open it through your browser's File > Open menu

3. **Or host it**:
Using Python's built-in server
python -m http.server 8000

Or using Node.js http-server
npx http-server


## 🎮 Usage

### Basic Controls
1. **Launch Fireworks**: Click anywhere on the canvas
2. **Auto Mode**: Click "Auto Launch" button to toggle continuous fireworks
3. **Sound Control**: Click "Sound: ON/OFF" to toggle audio
4. **Clear Display**: Click "Clear Canvas" to reset

### Keyboard Shortcuts
Currently, the application uses mouse/touch controls only. Keyboard shortcuts can be added as a future enhancement.

## 🛠️ Technologies Used

- **HTML5 Canvas**: For rendering graphics and animations
- **Vanilla JavaScript (ES6+)**: Core logic and physics engine
- **Web Audio API**: Real-time sound synthesis
- **CSS3**: UI styling with gradients and animations
- **RequestAnimationFrame**: Smooth 60fps animations

## 🎨 Customization

### Modify Firework Types
Edit the `types` array in the `launchFirework()` function:
const types = ['burst', 'ring', 'willow', 'mega', 'crackling'];

### Adjust Particle Count
Modify particle counts in the `explode()` method:
const particleCount = this.type === 'mega' ? 150 : 60;

### Change Colors
Edit the HSL values in color generation:
this.hue = Math.random() * 360; // Full spectrum
// Or limit to specific range:
this.hue = Math.random() * 60 + 30; // Yellow-orange range

### Adjust Sound Intensity
Modify gain values in sound functions:
bassGain.gain.setValueAtTime(0.8 * intensity, now); // Increase/decrease volume

### Auto Launch Speed
Change the interval in auto-launch mode:
autoLaunchInterval = setInterval(launchRandomFirework, 800); // milliseconds

## 📱 Browser Compatibility

| Browser | Minimum Version | Notes |
|---------|----------------|-------|
| Chrome | 34+ | Full support |
| Firefox | 29+ | Full support |
| Safari | 9+ | Full support |
| Edge | 12+ | Full support |
| Opera | 21+ | Full support |
| Mobile Safari | iOS 9+ | Full support |
| Chrome Mobile | Android 5+ | Full support |

## 🔧 Technical Details

### Performance
- Uses `requestAnimationFrame` for optimal rendering
- Efficient particle cleanup (removes faded particles)
- Canvas fade effect reduces memory overhead
- Typical performance: 60 FPS with 50-100 active particles

### Architecture
- **Object-Oriented Design**: Separate `Firework` and `Particle` classes
- **Modular Sound System**: Independent audio generation functions
- **Event-Driven**: Canvas click events trigger firework launches
- **State Management**: Maintains arrays for active fireworks and particles

## 🎯 Future Enhancements

- [ ] Add more firework types (fountain, roman candle, spinner)
- [ ] Implement keyboard controls
- [ ] Add particle collision detection
- [ ] Include preset color themes
- [ ] Add mobile touch gesture support for multi-firework launches
- [ ] Create recording/export functionality
- [ ] Add performance metrics display
- [ ] Implement wind effects for particle drift

## 🐛 Known Issues

- High particle counts (500+) may cause slowdown on older devices
- Safari on iOS may require user interaction before playing sounds
- Canvas size resets on window resize (particles are preserved)

## 📄 License

This project is free to use for personal and commercial purposes. Attribution appreciated but not required.

## 👨‍💻 Author

Created by a professional web developer for celebration and learning purposes.

## 🙏 Acknowledgments

- Inspired by real firework physics and pyrotechnics
- Web Audio API sound synthesis techniques
- HTML5 Canvas particle system patterns
- Community feedback and testing

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on the repository
- Contact the developer
- Check browser console for error messages

---

**Enjoy the show! 🎆✨🎇**

Made with ❤️ and JavaScript
