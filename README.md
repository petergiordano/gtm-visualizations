# GTM Visualizations

An interactive web application for Go-To-Market (GTM) market positioning analysis. This tool helps businesses understand how different customer personas value their product features through dynamic 2x2 grid visualizations.

🔗 **Live Demo**: https://gtm-visualizations.vercel.app

## Overview

The GTM Visualizations project provides:
- **Interactive 2x2 grid visualization** showing how companies position themselves based on product attributes
- **Dual-mode interface**:
  - **Demo Mode**: Pre-defined personas for manual simulation
  - **AI Mode**: AI-powered market analysis using Google Gemini API
- **Real-time clustering** of companies based on their attribute preferences
- **Visual highlighting** of target market segments

## Tech Stack

- **p5.js** (v1.9.0) - Interactive canvas visualizations
- **Tailwind CSS** (CDN) - Styling and responsive design
- **Google Gemini API** - AI-powered market analysis and persona generation
- **Vercel** - Deployment and hosting

## Local Development

Since this is a standalone HTML application, no build process is required:

1. Clone the repository:
```bash
git clone https://github.com/petergiordano/gtm-visualizations.git
cd gtm-visualizations
```

2. Open `positioning2x2sim.html` directly in your web browser

3. For AI features, add your Gemini API key in the code (positioning2x2sim.html:347)

## Deployment

### Vercel CLI Deployment

1. Install Vercel CLI globally (if not already installed):
```bash
npm install -g vercel
```

2. Login to Vercel:
```bash
vercel login
```

3. Deploy to Vercel:
```bash
vercel --yes
```

4. Deploy to production:
```bash
vercel --prod
```

### Vercel Web Deployment

This project is configured for automatic deployment via GitHub integration:

1. Push changes to the `main` branch
2. Vercel automatically deploys to production
3. View deployment at: https://gtm-visualizations.vercel.app

#### Vercel Configuration

The project includes a `vercel.json` file that configures:
```json
{
  "rewrites": [
    {
      "source": "/",
      "destination": "/positioning2x2sim.html"
    }
  ]
}
```

This ensures the main HTML file is served at the root URL.

## Project Structure

```
gtm-visualizations/
├── positioning2x2sim.html    # Main application file
├── CLAUDE.md                 # Instructions for Claude Code AI
├── fictional_product_content_posh.md  # Sample product data
├── vercel.json              # Vercel deployment configuration
├── .gitignore               # Git ignore file
└── README.md                # This file
```

## Environment Variables

For local development with Vercel CLI, create a `.env.local` file:
```
VERCEL_TOKEN=your_vercel_token_here
```

**Note**: The `.env.local` file is excluded from version control for security.

## Features

### Demo Mode
- Pre-configured customer personas
- Manual simulation controls
- Visual clustering of similar companies
- Highlighting of high-value target segments

### AI Mode
1. **Market Analyzer**: Analyzes product descriptions to extract key attributes
2. **Attribute Simulator**: Generates customer personas based on selected attributes
3. Real-time visualization of market positioning

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is proprietary. All rights reserved.

## Author

Peter Giordano

---

For more detailed technical information, see [CLAUDE.md](./CLAUDE.md).