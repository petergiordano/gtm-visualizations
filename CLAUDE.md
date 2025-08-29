# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a GTM (Go-To-Market) visualizations project that provides an interactive web application for market positioning analysis. The project consists of a single-page application that helps businesses understand how different customer personas value their product features.

## Architecture

The application is built as a standalone HTML file (`positioning2x2sim.html`) that integrates:
- **p5.js** (v1.9.0) - For interactive canvas visualizations
- **Tailwind CSS** (CDN) - For styling
- **Google Gemini API** - For AI-powered market analysis and persona generation

### Key Components

1. **Dual Mode Interface**:
   - **Demo Mode**: Pre-defined personas and manual simulation
   - **AI Mode**: AI-powered market analysis with two steps:
     - Market Analyzer: Analyzes product descriptions to extract attributes
     - Attribute Simulator: Generates customer personas based on attributes

2. **p5.js Visualization**:
   - Canvas-based 2x2 grid visualization (positioning2x2sim.html:463-739)
   - Company entities with animations and clustering behavior
   - Interactive highlighting of target zones

3. **AI Integration**:
   - Gemini 2.0 Flash model for analysis
   - Structured JSON responses with schema validation
   - Two main API calls:
     - Market analysis (positioning2x2sim.html:178-261)
     - Persona generation (positioning2x2sim.html:267-387)

## Development Commands

Since this is a standalone HTML file with no build process:
- **Run locally**: Open `positioning2x2sim.html` directly in a web browser
- **Deploy**: Upload the HTML file to any web server
- **Test**: Manual testing in browser (no test framework)

## Important Notes

1. **API Key**: The Gemini API key is currently empty in the code (positioning2x2sim.html:347). You'll need to add a valid API key for AI features to work.

2. **No Build Process**: This is a pure client-side application with CDN dependencies, so no npm/build commands are needed.

3. **Responsive Design**: The application adapts to mobile/desktop viewports using Tailwind's responsive utilities.

4. **State Management**: All state is managed within the p5.js sketch and JavaScript globals.