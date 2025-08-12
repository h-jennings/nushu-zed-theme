# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Zed Editor theme extension that ports the Nushu theme from VSCode. The theme is a fork of GitHub's default themes with alternative background colors for reduced contrast while maintaining the familiar Primer color palette.

## Architecture

### Core Files
- `extension.toml` - Extension manifest defining metadata, version, and theme contributions
- `themes/nushu-theme.json` - Main theme definition with both "Nushu Dark" and "Nushu Light" variants
- `icon.png` - Extension icon displayed in Zed's extension panel

### Reference Materials
- `vscode-reference/` - Original VSCode theme files for reference during development
- `gruvbox-reference/` - Gruvbox theme reference for comparison

### Theme Structure
The main theme file (`themes/nushu-theme.json`) follows Zed's theme schema v0.2.0 and contains:
- Two theme variants: "Nushu Dark" and "Nushu Light"
- Complete color definitions for all UI elements (background, borders, text, icons, etc.)
- Syntax highlighting colors for all language tokens
- Terminal color definitions
- Multi-player collaboration colors

## Development Commands

Since this is a theme extension with no build process, there are no specific build, test, or lint commands. Development involves:

1. **Testing changes**: Install as dev extension in Zed (Extensions panel > Install Dev Extension)
2. **Validation**: Ensure theme JSON follows Zed's schema at `https://zed.dev/schema/themes/v0.2.0.json`

## Theme Development Notes

### Color System
- Uses GitHub Primer color palette for syntax highlighting
- Dark theme: warm background tones (#25211d base, #2b2723 surfaces)
- Light theme: cream background tones (#f8f6f1 base, #efede9 surfaces)
- Accent colors: Blue (#1f6feb dark, #0969da light) for primary actions

### Key Design Principles
- Reduced contrast compared to standard GitHub themes
- Maintains familiarity through consistent syntax colors
- Warm-toned backgrounds for comfortable extended use

### Syntax Token Coverage
The theme provides comprehensive syntax highlighting for:
- Basic tokens (keywords, strings, numbers, comments)
- Language-specific constructs (functions, types, attributes)
- Markup elements (emphasis, links, titles)
- Special cases (escape sequences, regex, predictive text)