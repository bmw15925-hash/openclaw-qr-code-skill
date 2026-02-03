# QR Code Skill for OpenClaw

Generate and read QR codes directly from your AI assistant.

## Features

- 📝 **Generate QR codes** from any text, URL, or data
- 📷 **Read QR codes** from image files (PNG, JPG, screenshots)
- ⚙️ **Customizable** size, border, and error correction levels
- 🖼️ **Multiple formats** supported for input images

## Installation

```bash
# Install the skill
openclaw skills install qr-code

# Install Python dependencies
pip install qrcode pillow pyzbar
```

### Platform-specific requirements for QR reading:

- **Windows**: Install [Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe)
- **macOS**: `brew install zbar`
- **Linux**: `apt install libzbar0`

## Usage

### Generate a QR Code

```
"Create a QR code for https://github.com"
"Generate QR code with my WiFi password: MyPassword123"
"Make a QR code for my contact info"
```

### Read a QR Code

```
"Read the QR code in this image"
"What does this QR code say?"
"Decode the QR code from screenshot.png"
```

## Command Line

```bash
# Generate
python scripts/qr_generate.py "Hello World" output.png

# Generate with options
python scripts/qr_generate.py "https://example.com" qr.png --size 15 --error H

# Read
python scripts/qr_read.py image.png

# Read with JSON output
python scripts/qr_read.py image.png --json
```

## License

MIT License - Omar Khaleel
