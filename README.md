# DeepView - Trading Terminal & Command Center

![Full screen logo](https://github.com/user-attachments/assets/a34bf806-8fab-4bf9-959d-741a738a420b)


**DeepView** is a powerful, browser-based trading dashboard and command center inspired by the Bloomberg Terminal. Built for traders and analysts who need real-time market intelligence, multi-screen layouts, and seamless workflow management - all in one desktop application.

---

## Why DeepView?
- Most traders use: 10+ browser tabs, multiple charting tools, and several data websites.
- **DeepView solves this by creating a single unified trading workspace.**

## With DeepView, you can:

* ✔ Monitor multiple markets simultaneously
* ✔ Compare charts side-by-side
* ✔ Track big trades & liquidations
* ✔ Journal your trading decisions
* ✔ Launch trading tools instantly
* ✔ Create multi-screen trading setups

## ✨ Features

- **Home** — Live Charts, Order Blocks, Liquidations, Big Trades, News, Market Screeners, Historical Charts, and Footprint Charts
- **Multi-Panel Dashboard** — Split-screen layouts with configurable URL panels for simultaneous market monitoring
- **Multi-Screen Tabs** — Create multiple workspaces (windows) with independent 3-panel layouts, switch between them like browser tabs
- **Advanced Charting** — Integrated TradingView-style charts powered by Cryexc with full technical analysis tools
- **Multi-Chart View** — 2×2 grid layout for comparing multiple charts side-by-side
- **Trading Journal** — Built-in journal to log trades, strategies, and market observations
- **Drawing Board** — Freehand drawing canvas for sketching trade setups and market analysis
- **Apps Drawer** — Quick-access overlay to launch trading tools (TradingView, Investing.com, ForexFactory, YouTube, etc.) as floating draggable windows
- **Persistent Sessions** — All panel URLs and workspace configurations are saved and restored automatically


## 🖥️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18, TypeScript 5, Vite 5 |
| **Styling** | Tailwind CSS 3, shadcn/ui components |
| **Desktop Runtime** | Electron (Chromium-based) |
| **Routing** | React Router v6 |
| **State** | React hooks + localStorage persistence |
| **Charts** | Cryexc project and TradingView charting engine |
| **Panels** | react-resizable-panels |

## 📁 Project Structure

```
├── electron/
│   └── main.cjs            # Electron main process
├── public/
│   └── app-icon.png         # Application icon
├── src/
│   ├── assets/              # Icons, images, GIFs
│   ├── components/
│   │   ├── pages/           # Page components (Home, Chart, Journal, etc.)
│   │   ├── ui/              # shadcn/ui primitives
│   │   ├── AppsDrawer.tsx   # Floating apps overlay
│   │   ├── PanelFrame.tsx   # URL panel with controls
│   │   ├── Sidebar.tsx      # Navigation sidebar
│   │   ├── SplashScreen.tsx # Startup animation
│   │   └── TopBar.tsx       # Window title bar
│   ├── hooks/               # Custom React hooks
│   └── pages/               # Route-level pages
├── electron-release/        # Packaged desktop builds
└── vite.config.ts
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm or bun

### Development

```bash
# Install dependencies
npm install

# Start dev server (browser)
npm run dev

# Start Electron dev mode
npx electron .
```

### Build for Production

```bash
# Build frontend
npx vite build

# Package Windows desktop app
npx @electron/packager . DeepView --platform=win32 --arch=x64 --out=electron-release --overwrite --ignore='node_modules' --ignore='^/src' --ignore='^/public' --ignore='^/electron-release'
```


| Home Dashboard | Multi-Screen | Charts |
|:-:|:-:|:-:|
| Real-time market overview | Tabbed multi-panel workspaces | Full technical analysis |

## 📋 Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + K` | Quick command |


---

<p align="center">
  <b>DeepView</b> — Your all-in-one trading command center.
</p>
