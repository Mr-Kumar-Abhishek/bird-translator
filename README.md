# Bioacoustic Sparrow Analyzer

A web-based bioacoustic analysis tool for analyzing bird sound patterns and audio signatures. This application provides real-time audio visualization and analysis capabilities with offline support.

## Features

- **Real-Time Audio Visualization**: Visual waveform and frequency analysis of bird sounds
- **Dark-Themed Interface**: Professional, easy-on-the-eyes dark UI optimized for extended use
- **Progressive Web App (PWA)**: Install as a standalone app on desktop and mobile devices
- **Offline Support**: Works offline through service worker caching
- **Mobile Optimized**: Responsive design that works seamlessly across devices
- **Audio Data Readout**: Display key audio metrics and analysis data

## Getting Started

### Prerequisites

- Modern web browser with Web Audio API support
- Microphone access (for real-time analysis)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Mr-Kumar-Abhishek/bird-translator.git
cd bird-translator
```

2. Open in a web browser:
   - Simply open `index.html` in your browser
   - Or serve through a local web server: `python -m http.server 8000`

3. Install as PWA (optional):
   - Click the install banner that appears in the browser
   - Or use your browser's "Install app" option

## Usage

1. **Grant Microphone Access**: Allow the application to access your microphone when prompted
2. **Analyze Audio**: The application will display real-time visualization of incoming audio
3. **Review Data**: Check the readout panel for audio metrics and analysis

## Technical Details

- **Frontend**: HTML5, CSS3, JavaScript (vanilla)
- **Audio Processing**: Web Audio API
- **Offline Support**: Service Worker with Cache-First strategy
- **Responsive Design**: Mobile-first CSS with Flexbox/Grid layout

## Features Used

- Canvas API for audio visualization
- Web Audio API for audio analysis
- Service Worker API for offline functionality
- Web App Manifest for PWA installation
- Responsive viewport meta tags

## COCOMO Cost Estimation

A Constructive Cost Model (COCOMO) estimation has been performed for this project. Assuming a 50 KLOC project size and an average salary of $8,000 USD per Person-Month, the estimated costs across the three project types are:

- **Organic (Simple)**: 145.02 Person-Months (~9 Persons) | **Cost**: $1,160,160 USD
- **Semi-detached (Medium)**: 244.02 Person-Months (~15 Persons) | **Cost**: $1,952,160 USD
- **Embedded (Complex)**: 393.61 Person-Months (~23 Persons) | **Cost**: $3,148,880 USD

For the detailed breakdown and formulas, see the [cocomo_calculations.md](cocomo_calculations.md) file.

## License

All Rights Reserved. © 2026

This software and all its contents are protected by copyright. No part of this project may be reproduced, distributed, or transmitted in any form or by any means without prior written permission from the copyright holder.

## Author

Mr. Kumar Abhishek
