# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Architecture

This repository contains an audio conversion desktop application built with Tauri, combining a React frontend with a Rust backend. The main application is located in the `claude-code-tauri/` directory.

### Application Purpose
An audio file conversion tool with a tabbed interface featuring:
- **Input Tab**: File selection with drag-and-drop, displaying file details (name, size, format, path, modification date)
- **Output Settings Tab**: Comprehensive conversion options including output location, folder organization, file naming (prefix/suffix, date stamps, text replacement), format selection, and quality settings (bitrate/file size targets)
- **Settings Tab**: Configuration for supported audio file formats

### Technology Stack
- **Framework**: Tauri 2.0
- **Frontend**: React 19.1.0 + TypeScript + Vite (runs on port 1420)
- **CSS**: Tailwind CSS (as specified in requirements)
- **Backend**: Rust with Tauri 2.0 framework
- **Build System**: Vite for frontend, Cargo for Rust backend
- **Window**: 800x600px desktop application

## Development Commands

### Frontend Development
```bash
cd claude-code-tauri
npm run dev          # Start development server
npm run build        # Build for production (runs tsc && vite build)
npm run preview      # Preview production build
```

### Tauri Desktop App
```bash
cd claude-code-tauri
npm run tauri dev    # Run Tauri app in development mode
npm run tauri build  # Build desktop application
```

## Environment Setup

- Git Bash path configured via `claude_env.ps1`: `c:\Users\BIKO-MINI\scoop\shims\bash.exe`

## Application Details

The audio conversion application uses Tauri's IPC system for communication between the React frontend and Rust backend. The current implementation includes a basic `greet` command, but the application architecture is designed to support audio file processing, format conversion, and file management operations as described in the Japanese specification document.