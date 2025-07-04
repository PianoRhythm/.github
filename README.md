# PianoRhythm

PianoRhythm is a multiplayer social web application that allows users to play music and casual games with people from around the world. Experience real-time musical collaboration with advanced 3D rendering, custom synthesizers, and seamless cross-platform support.

🎹 **[Try PianoRhythm Live](https://pianorhythm.github.io/pianorhythm-ssr/)** | 🌐 **[Main Site](https://pianorhythm.io)** | 📚 **[Documentation](https://docs.pianorhythm.io)**

## About the Project

PianoRhythm is designed to create a collaborative musical experience where users can:

- **Play music together in real-time** with low-latency synchronization
- **Interact through chat and social features** with typing indicators and user profiles
- **Join or create themed rooms** with customizable environments
- **Participate in casual games** including rhythm games and musical challenges
- **Customize their experience** with multiple themes, 3D/2D rendering modes, and UI preferences
- **Use MIDI devices** for authentic piano playing experience

## Technical Architecture

### Frontend
- **Framework**: SolidJS with Server-Side Rendering (SSR)
- **Language**: TypeScript
- **Real-time Communication**: WebSockets, WebRTC
- **UI Components**: Hope UI (custom fork)
- **State Management**: Solid Services, Immer
- **Build System**: Vinxi with custom presets
- **Testing**: Vitest, Solid Testing Library, Cypress

### Backend
- **Runtime**: Bun (production), Node.js (development)
- **Real-time Server**: WebSocket with crossws adapter
- **Database**: MongoDB with Data API
- **API**: REST endpoints with server middleware
- **Authentication**: OAuth (Discord, GitHub) with JWT

### Core Engine
- **Language**: Rust (Nightly toolchain)
- **Integration**: WebAssembly with wasm-bindgen
- **Serialization**: Protocol Buffers
- **Audio**: Custom synthesizer implementation with Web Audio API
- **3D Rendering**: Bevy Engine 0.16 (WebGPU/WebGL2)
- **MIDI Support**: Web MIDI API integration

### Cross-Platform Support
- **Web Application**: Primary platform with GitHub Pages deployment
- **Desktop Application**: Tauri-based native wrapper
- **Environment Detection**: Adaptive features based on platform
- **Mobile Support**: Responsive design with touch controls

### Initialization System
- **Architecture**: Dependency-based state machine for reliable startup
- **Race Condition Prevention**: Eliminates timing-dependent initialization failures
- **Error Recovery**: Retry mechanisms and timeout handling for robust operation
- **Progress Tracking**: Real-time initialization progress with detailed logging

## Key Features

### Music Collaboration
- **Real-time MIDI synchronization** with sub-100ms latency
- **Advanced synthesizer** with custom Rust-based audio engine
- **Multi-instrument support** with realistic piano physics
- **Sheet music integration** with interactive score display
- **Recording and playback** capabilities

### Social Interaction
- **Room-based collaboration** with up to 16 simultaneous players
- **Real-time chat** with typing indicators and emoji support
- **User profiles** with customizable avatars and statistics
- **Friend system** with online status and invitations
- **Admin dashboard** for room management

### User Experience
- **Multiple themes** with dark/light mode support
- **Internationalization (i18n)** with multi-language support
- **3D and 2D rendering modes** powered by Bevy Engine
- **Responsive design** optimized for desktop and mobile
- **Accessibility features** with keyboard navigation

### Technical Features
- **Comprehensive error handling** with user-friendly feedback
- **Automated testing** with 90%+ code coverage
- **CI/CD pipeline** with self-hosted runners
- **Performance monitoring** with real-time metrics

## Deployment

### GitHub Pages (Current)
The project is automatically deployed to GitHub Pages on every push to the main branch:
- **Live Demo**: https://pianorhythm.github.io/pianorhythm-ssr/
- **Deployment**: Automatic via GitHub Actions
- **Build**: Static site generation with SSR prerendering

### Production Deployment
For production environments, the application is deployed using:
- **Container Registry**: DigitalOcean Container Registry
- **Runtime**: Bun server with Docker containers
- **CDN**: Custom assets and static content delivery
- **Database**: MongoDB Atlas with Data API

## Building

The project uses **Vinxi** with custom presets for different deployment environments:

- **Development**: Hot reload with source maps
- **Staging**: Optimized build with debugging enabled
- **Production**: Fully optimized with prerendering and minification

### Test Coverage
- **Frontend**: Vitest with Solid Testing Library
- **Components**: Snapshot and interaction testing
- **Services**: Mock-based unit testing
- **E2E**: Cypress for full user workflows

### Initialization System Development
When working with the app initialization:
- **Adding new steps**: Follow the dependency-based pattern in `InitializationService`
- **Race condition prevention**: Always use the initialization service for startup operations
- **Testing**: Write tests for new initialization steps using the established patterns
- **Debugging**: Use the comprehensive logging system for troubleshooting startup issues

## Acknowledgments

- Built with [SolidJS](https://solidjs.com/) and [Vinxi](https://vinxi.vercel.app/)
- 3D rendering powered by [Bevy Engine](https://bevyengine.org/)
- Audio synthesis with custom Rust implementation
- UI components based on [Hope UI](https://hope-ui.com/)

---

**PianoRhythm** - Bringing people together through music 🎹✨
