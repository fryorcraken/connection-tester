# Waku Connection Tester

A simple HTML static website that uses @waku/sdk via CDN to monitor Waku node connections in real-time.

## Features

- Creates a Waku light node and connects to the network
- Real-time graph showing connection counts over time
- Separate tracking for different protocols:
  - Store Protocol
  - Light Push Protocol
  - Filter Protocol
  - Total connections
- Live connection status display
- Activity logs

## Setup

**No installation required!** This is a static HTML file that works directly in the browser.

### Option 1: Simple HTTP Server
```bash
npm run dev
```
Then open `http://localhost:8080/?v=0.0.33`

You can change the version of the Waku SDK used with the `v` query parameter.
For example: `http://localhost:8080/?v=0.0.33`

### Option 2: Direct File Access
Simply open `index.html` directly in your browser (some browsers may block CDN imports for file:// URLs)

### Option 3: Any HTTP Server
```bash
# Python 3
python3 -m http.server 8080

# Python 2
python -m SimpleHTTPServer 8080

# Node.js (if you have http-server installed globally)
npx http-server -p 8080
```

## Usage

1. Click "Start Node" to create and start the Waku node
2. Wait for the node to connect to remote peers
3. Monitor the real-time graph showing connection counts
4. View protocol-specific connection statistics
5. Check the logs for detailed activity information

## Technical Details

- Uses @waku/sdk via unpkg.com CDN
- Chart.js for real-time graph visualization
- Pure HTML/CSS/JavaScript - no build process needed
- Monitors libp2p connections and peer protocols
- Updates every 2 seconds
- Completely self-contained in a single HTML file

## Browser Requirements

- Modern browser with ES modules support
- WebRTC support for peer-to-peer connections
- Internet connection to load CDN dependencies
- HTTPS or localhost (required for WebRTC)