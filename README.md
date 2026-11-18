# Glacier tilt viewer

Live: https://braakhekke.github.io/tilt/

Eleven exact-date CDSE Sentinel-2 Level-1C scenes per glacier (Aletsch and Rhône), 2016–2026, exported through Tongues from Space with the Copernicus Browser true-colour optimized recipe. All years use the same crop. `imagery.json` and `rhone-imagery.json` record dates, orbit, rendering parameters and checksums.

Starts at 2021. Tap to enable motion on a phone. Tilt the top edge away to advance; tilt it towards you to go back. Swipe up/down or use arrow keys as a fallback. Double-tap to return to 2021.

Static GitHub Pages deployment from the root of `main`; no API keys or external runtime dependencies. The 1080×1920 frames cover a portrait phone viewport; landscape preserves the full portrait image.

Imagery: modified Copernicus Sentinel data, via CDSE. Export pipeline: Tongues from Space, Jochem Braakhekke.

The three-dot button opens the glacier picker. Tilt pauses while the picker is open. Selecting a glacier resets to 2021, retains motion permission, and updates the shareable URL (`#aletsch` or `#rhone`). Only the active glacier is preloaded; switching releases the previous decoded frames.

Controls fade when the phone is still. Tap the image to reveal the year and glacier selector. The small north-up scale is calibrated separately for each crop (`scale-calibration.json`) and recomputed from the image’s actual cover scaling on resize. Source-map scale widths are rounded to CSS pixels, so ground distances are approximate. Typography uses Avenir Next/Avenir where available with system fallbacks, for controls, dates and glacier names.

Pinch to zoom (1×–4×); use two fingers to pan. One-finger vertical swipes still change the year. Zoom and pan stay fixed across years, reset on glacier selection, and the metric scale updates at every zoom level. Double-tap resets the view and year to 2021.

The small circular-arrow button recenters motion at the current phone posture and returns to 2021, preserving zoom. Tilt spans about 24° from 2016 to 2026 (2.4° per year), with smoothing and hysteresis to keep frames steady. Tap the image to reveal the reset control.

Top-left local names and country/canton accompany a frameless GLAMOS 2023 overview. Its approximate image footprint follows cover cropping, pinch zoom and pan. See locator-provenance.json. Identity, overview, north arrow and reset fade with the year; the glacier picker and metric scale remain visible.
