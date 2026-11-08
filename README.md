# Ale, My Eyes! - PC

Desktop application for the Ale, My Eyes! visual assistant.

## Overview

This repository contains the desktop (Windows/Linux) version of the Ale, My Eyes! application, including:

- **ale-gui**: Graphical user interface with screen capture and desktop automation
- **ale-cli**: Command-line interface for terminal-based usage
- **ale-core**: Core library (shared via git submodule from [ale-my-eyes-core](https://github.com/risalydevclub/ale-my-eyes-core))

## Features

- Voice-activated visual assistance
- Screen capture and analysis
- Desktop automation (click, type, scroll)
- Text-to-speech responses
- Cloud API integration (OpenAI GPT-4o, Whisper, TTS)

## Building

### Prerequisites

- Rust toolchain (stable)
- Linux dependencies: `libspeechd-dev libasound2-dev libfontconfig-dev libpipewire-0.3-dev libwayland-dev libxrandr-dev libdbus-1-dev libegl-dev libgbm-dev libxcb-shape0-dev libxcb-xfixes0-dev libclang-dev`

### Build

```bash
# Initialize submodule
git submodule update --init --recursive

# Build GUI
cargo build --release -p ale-gui

# Build CLI
cargo build --release -p ale-cli
```

## Usage

```bash
# Run GUI
cargo run --release -p ale-gui

# Run CLI
cargo run --release -p ale-cli -- transcribe audio.wav
cargo run --release -p ale-cli -- synthesize "Hello world"
cargo run --release -p ale-cli -- describe image.jpg
```

## Related Projects

- [ale-my-eyes-core](https://github.com/risalydevclub/ale-my-eyes-core) - Core library
- [ale-my-eyes-android](https://github.com/risalydevclub/ale-my-eyes-android) - Android application

## License

MIT
