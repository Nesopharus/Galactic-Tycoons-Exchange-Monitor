# Galactic-Tycoons-Exchange-Monitor

Single-page HTML application for near real-time monitoring of the Galactic Tycoons material exchange. Compares current market prices against averages and alerts when prices deviate significantly.

## Features

- **Two monitoring modes:** Entire market or only materials from a personal wishlist
- **Deviation alerts:** Configurable threshold (%) — toast notification and audio beep when breached
- **API cost tracking:** Rolling 10-minute window to stay within the rate limit (500 points / 10 min)
- **Rate-limit protection:** Automatic pause on HTTP 429 or self-detected limit breach with countdown display
- **Persistent settings:** API key and parameters are saved in the browser's localStorage

## Usage

Open `galactic-monitor.html` directly in a browser.
No server or build step required.

1. Enter your Galactic Tycoons API key
2. Configure fetch interval, wishlist interval, and alert threshold
3. Select mode: **All Materials** or **Wishlist**
4. Click "Start"
