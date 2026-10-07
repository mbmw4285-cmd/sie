# VERDIX Groq AI Web App

Uses the browser webcam, Groq Vision AI, and an ESP32 sorting endpoint.

## Run
1. Install Node.js.
2. Open terminal in this folder and run `npm install`.
3. Copy `.env.example` to `.env`.
4. Put your Groq API key in `.env`.
5. Optionally set `ESP32_URL=http://YOUR_ESP32_IP`.
6. Run `npm start`.
7. Open `http://localhost:3000` and allow camera access.

The API key stays on the Node.js server; it is never put in browser code.

## ESP32 API
The server POSTs to `http://YOUR_ESP32_IP/sort`:
`{"material":"PLASTIC"}`

Map PLASTIC/PAPER/METAL/ORGANIC to your servo positions in the ESP32 firmware.

Groq Vision is used for general image understanding; test carefully before driving physical hardware.
