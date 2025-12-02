# 🧠 Mindora - AI Mind Map Generator

<p align="center">
  <img src="assets/logo.svg" width="120" height="120" alt="Mindora Logo">
</p>

<p align="center">
  <strong>Transform articles into beautiful, interactive mind maps with AI</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#demo">Demo</a> •
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#chrome-extension">Chrome Extension</a> •
  <a href="#development">Development</a>
</p>

---

## ✨ Features

### 🎯 Core Features
- **One-click Mind Map Generation** - Paste any article and get a structured mind map instantly
- **AI-Powered Analysis** - Uses Claude AI to extract key concepts and relationships
- **Language Preservation** - Maintains original language (Chinese→Chinese, English→English)
- **Interactive Canvas** - Drag, zoom, and pan your mind map

### 🖱️ Multi-Select & Batch Operations
- **Direct Box Selection** - Click and drag to select multiple nodes (no keyboard shortcuts needed!)
- **Batch Move** - Move all selected nodes together by dragging any one
- **Shift/Cmd+Click** - Add/remove individual nodes from selection

### 🎨 Comprehensive Color System
- **18 Text Colors** - From subtle grays to vibrant accent colors
- **18 Background Colors** - Both dark and light variants
- **Auto Color Similar** - Automatically group similar content with matching colors
- **Per-Node Customization** - Right-click any node to change its colors

### 🌓 4 Theme Modes
| Theme | Description |
|-------|-------------|
| **Dark** | Deep blue-black background, perfect for night use |
| **Light** | Clean white background for daytime |
| **Blue** | Tech-inspired deep blue theme |
| **Sepia** | Warm beige tones for eye comfort |

### 📝 Notion-Style Formatting
- Text, Headings (H1/H2/H3)
- Bullet & Numbered Lists
- Todo Lists with checkboxes
- Quotes & Code blocks

---

## 🎬 Demo

![Mindora Demo](assets/demo.gif)

### Screenshots

<table>
  <tr>
    <td><img src="assets/screenshot-dark.png" alt="Dark Theme"></td>
    <td><img src="assets/screenshot-light.png" alt="Light Theme"></td>
  </tr>
  <tr>
    <td align="center">Dark Theme</td>
    <td align="center">Light Theme</td>
  </tr>
</table>

---

## 📦 Installation

### Web App (React)

```bash
# Clone the repository
git clone https://github.com/yourusername/mindora.git
cd mindora

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

### Chrome Extension

1. Download or clone this repository
2. Open Chrome and go to `chrome://extensions/`
3. Enable "Developer mode" (top right)
4. Click "Load unpacked"
5. Select the `chrome-extension` folder
6. Click the Mindora icon and enter your Claude API key

---

## 🚀 Usage

### Web App

1. **Open the app** in your browser
2. **Paste your article** into the text area
3. **Click "Generate Mind Map"** and wait for AI analysis
4. **Interact** with your mind map:
   - Drag nodes to reposition
   - Click and drag on empty space to box-select
   - Right-click for context menu
   - Scroll to zoom
   - Use the theme selector to change appearance

### Chrome Extension

1. **Select text** on any webpage
2. **Right-click** and choose "Generate Mind Map with Mindora"
3. Or right-click anywhere and choose "Generate Mind Map from Page"
4. View, edit, and export your mind map

---

## 🗂️ Project Structure

```
mindora/
├── src/
│   ├── App.jsx           # Main React application
│   ├── main.jsx          # Entry point
│   └── index.css         # Global styles
├── chrome-extension/
│   ├── manifest.json     # Extension manifest
│   ├── background.js     # Service worker
│   ├── content.js        # Content script
│   ├── content.css       # Content styles
│   ├── popup/
│   │   ├── popup.html    # Popup UI
│   │   └── popup.js      # Popup logic
│   └── icons/            # Extension icons
├── assets/
│   ├── logo.svg          # Logo files
│   └── screenshots/      # Documentation images
├── package.json
├── vite.config.js
└── README.md
```

---

## 🛠️ Development

### Prerequisites
- Node.js 18+
- npm or yarn
- Claude API key (get one at [console.anthropic.com](https://console.anthropic.com))

### Tech Stack
- **Frontend**: React 18, Vite
- **Styling**: Inline styles (no external CSS framework)
- **AI**: Anthropic Claude API
- **Extension**: Chrome Manifest V3

### Available Scripts

```bash
# Development
npm run dev        # Start dev server

# Build
npm run build      # Build for production
npm run preview    # Preview production build

# Linting
npm run lint       # Run ESLint
```

### Environment Variables

Create a `.env` file for local development:

```env
VITE_CLAUDE_API_KEY=your-api-key-here
```

---

## 🎨 Color Reference

### Text Colors
```
Gray: #9ca3af    Red: #f87171     Orange: #fb923c
Yellow: #fbbf24  Green: #4ade80   Cyan: #22d3ee
Blue: #60a5fa    Purple: #c084fc  Pink: #f472b6
```

### Background Colors (Dark)
```
Gray: #374151    Red: #7f1d1d     Orange: #78350f
Yellow: #713f12  Green: #14532d   Cyan: #164e63
Blue: #1e3a8a    Purple: #581c87  Pink: #831843
```

### Background Colors (Light)
```
Red: #fecaca     Orange: #fed7aa  Yellow: #fef08a
Green: #bbf7d0   Cyan: #a5f3fc    Blue: #bfdbfe
Purple: #ddd6fe  Pink: #fbcfe8
```

---

## 📄 API Reference

### Mind Map Data Structure

```json
{
  "title": "Main Topic",
  "summary": "One sentence summary",
  "customColor": "#fecaca",
  "textColor": "#7f1d1d",
  "branches": [
    {
      "title": "Branch Title",
      "format": "text",
      "customColor": "#a5f3fc",
      "textColor": "#164e63",
      "children": [
        {
          "title": "Child Item",
          "note": "Optional note",
          "format": "bullet",
          "todoChecked": false
        }
      ]
    }
  ]
}
```

### Format Types
- `text` - Plain text
- `h1`, `h2`, `h3` - Headings
- `bullet` - Bullet list
- `number` - Numbered list
- `todo` - Todo with checkbox
- `quote` - Quote block
- `code` - Code block

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Anthropic Claude](https://www.anthropic.com/) for the AI capabilities
- [Zettelkasten Method](https://zettelkasten.de/) for inspiration
- [Notion](https://notion.so) for UI/UX inspiration

---

<p align="center">
  Made with ❤️ by the Mindora Team
</p>
