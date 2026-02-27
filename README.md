# Virage Race

Single-page WebHID app for reading RC transponder passings from CP2110-based decoders (EasyLAP / Robitronic) and displaying live race stats.

## What it does

- Connects to a CP2110 HID-UART device directly from the browser (no desktop app).
- Parses passings and shows them in real time.
- Tracks race state: start, stop, reset.
- Calculates lap metrics per transponder (laps count, last lap, best lap, average lap, total time).
- Stores transponder names in browser local storage.
- Includes raw log and hex dump views for diagnostics.

## Requirements

- Google Chrome or Microsoft Edge (version 89+).
- WebHID support enabled in the browser.
- A compatible CP2110-based decoder connected via USB.

## Use online

- Live app: https://rai220.github.io/virage-race/

## Run locally

This project is a single HTML file with inline CSS/JS.

1. Open `index.html` in a supported browser.
2. Click connect and select your CP2110 device in the browser dialog.
3. Start race tracking and pass cars through the loop/frame.

If direct file opening is restricted in your environment, serve the folder with any static HTTP server and open the served page.

## Project structure

- `index.html` - complete application UI and logic.

## Notes

- The interface text is currently in Russian.
- Browser support is intentionally limited to engines with WebHID.
