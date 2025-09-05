# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Easy Typer (木易跟打器) is a macOS typing practice application built with Vue.js 2, TypeScript, and Electron. It's designed for Chinese Wubi input method users to practice typing by loading text from QQ chat and providing real-time feedback.

## Key Technologies
- **Frontend**: Vue.js 2 with TypeScript, Vuex, Vue Router
- **UI Framework**: Element UI
- **Desktop**: Electron for macOS packaging
- **Build**: Vue CLI 4.5
- **Database**: IndexedDB for local data storage
- **Styling**: SCSS with dark/light theme support

## Development Commands

```bash
# Install dependencies
yarn install

# Development server with hot-reload
yarn serve

# Build for production
yarn build

# Run unit tests
yarn test:unit

# Lint and fix files
yarn lint

# Electron development
yarn start

# Build Electron app
yarn dist

# Package for macOS
yarn package-mac
```

## Project Structure

```
src/
├── components/          # Vue components
│   ├── Racing.vue      # Main typing interface
│   ├── Article.vue     # Article display
│   └── Words.vue       # Word suggestions
├── store/              # Vuex stores
│   ├── racing.ts       # Typing state management
│   ├── article.ts      # Article management
│   └── util/           # Utility functions
├── views/              # Page components
│   ├── Home.vue        # Main homepage
│   ├── Setting.vue     # Application settings
│   └── History.vue     # Typing history
├── api/                # API interactions
└── assets/             # Styles and fonts

electron/
├── main.js             # Electron main process
├── preload.js          # Preload scripts
└── bin/                # Binary dependencies
```

## Key Features
- QQ chat text loading via F4 shortcut
- Real-time typing statistics (speed, accuracy, keystrokes)
- Word suggestion and coding hints for Wubi input
- Local history and achievement tracking
- Dark/light theme support
- Electron-based desktop application

## Development Notes
- Uses Vue Class Component decorators for TypeScript
- IndexedDB for local data persistence
- AppleScript integration for QQ text retrieval on macOS
- Custom keyboard handling and input analysis
- Performance monitoring with heatmap.js integration

## Testing
- Jest unit tests with Vue Test Utils
- ESLint with Standard and TypeScript rules
- Pre-commit hooks with lint-staged

## Build Configuration
- Vue CLI 4.5 with custom webpack configuration
- TypeScript 3.9 with experimental decorators
- Electron Builder for desktop packaging
- PWA capabilities for web deployment