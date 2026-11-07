# J.A.R.V.I.S. Personal HUD

A mobile-first electric-blue JARVIS-inspired interface for Android browsers. Static site; no root, backend, or account required.

## Features
- Animated arc-reactor visual and responsive HUD
- Touch command console, quick actions, fullscreen
- Voice input where the browser supports Web Speech API
- Optional MediaPipe hand tracking, loaded only after the user taps Hand Tracking
- PWA manifest and service-worker caching
- Battery/network status only where browser APIs expose them

## Limitations and privacy
This is a visual browser interface, not an Android system controller or full AI assistant. Webpages cannot reliably read Android CPU temperature, total RAM usage, battery health, or control system settings. The interface does not invent those values.

Hand tracking requires HTTPS, camera permission, a compatible browser, and internet access to load MediaPipe scripts/model initially. Camera frames are processed for live landmarks in the page; this project does not record or upload footage. Switching away stops the camera. Voice recognition varies by browser and may use the browser vendor's speech service.

## Deploy
In repository Settings → Pages, select GitHub Actions as the deployment source. The included workflow deploys on pushes to main. Expected URL: https://rahul-dev-git0.github.io/jarvis-vivo-hud/

## Install on Vivo V70
Open the HTTPS site in Chrome → menu → Add to Home screen / Install app. Launch its icon for a standalone HUD. It does not replace the Android launcher or lock screen. Enable Hand Tracking only when you want camera gestures.

## Commands
Type help, time, date, scan, fullscreen, camera. Open palm triggers a scan; pinch changes the accent colour.

## License
MIT. See LICENSE.