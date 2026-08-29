# 📜 Changelog

All notable changes to the **Mikes 420 Grindhouse App** suite are documented in this file.

---

## [v1.8.0] - Build 39 (2026-08-29)
### 💬 Subtitles & Closed Captioning (CC)
- **Universal Subtitle Support:** Native parsing and rendering of CyTube subtitle tracks (`.vtt`, `.srt`, `.ass`, `.ttml`) for direct streams in ExoPlayer/Media3.
- **Dedicated Subtitles Toggle:** Added persistent *Untertitel (CC)* / *Subtitles (CC)* switch under Playback settings (*Wiedergabe*) with state persistence across app restarts.
- **High-Contrast TV & Mobile Styling:** Configured native `SubtitleView` with high-contrast white text, transparent background, and crisp black outline for optimal legibility on both TVs and mobile displays.
- **Real-Time Stream Sync:** Dynamically switches ExoPlayer text tracks and YouTube CC policies without interrupting video or audio playback.

---

## [v1.7.0] - Build 38 (2026-08-23)
### 🎬 Features & UI Polish
- **Clean Title Recognition:** Now playing overlay displays cleanly formatted movie or series titles with seamless raw stream filename fallback.
- **Scrollable EPG Queue:** Up-next queue list is now fully scrollable (up to 50 scheduled items) via TV remote D-Pad (▲ / ▼).
- **Start Times & Cleaner Queue:** Removed numbered index prefixes (`1.`, `2.`, `3.`) from queue rows and quick HUD; displayed exact broadcast start times (e.g. `21:45`) instead.
- **Facts Renaming:** Renamed movie metadata section from `"TRIVIA"` to `"ADDITIONAL FACTS"` / `"ZUSÄTZLICHE FAKTEN"`.

---

## [v1.6.8] - Build 36 (2026-08-21)
### 🛠️ Fixed
- **Seamless Stream Transitions:** Resolved video player getting stuck in a paused state when transitioning between YouTube interludes and live direct streams.

---

## [v1.6.7] - Build 35 (2026-08-21)
### 🛠️ Fixed
- **Video Freeze Resolution:** Eliminated recurring video freezes caused by repetitive hardware decoder flushes on Fire TV and Android TV devices.
- **Adaptive Multi-Tier Speed Nudging:**
  - Continuous drift reconciliation now uses smooth playback speed adjustment (`1.02x` to `1.12x`) without restarting or flushing the hardware decoder pipeline.
  - Raised hard `seekTo` threshold to 120 seconds (reserved exclusively for large manual skips or playlist jumps).
  - Extended startup grace period to 25s, allowing media streams and decoder buffers to stabilize cleanly.

---

## [v1.6.6] - Build 34 (2026-08-21)
### ⚡ Optimized
- **Buffer & Decoder Stability:** Enhanced ExoPlayer / Media3 decoder lifecycle management on MediaTek and ARM TV chipsets.
- **Build Infrastructure:** Updated Gradle & Kotlin toolchains for faster native compilation and smaller release bundle footprints.

---

## [v1.6.5] - Build 33 (2026-08-20)
### ⚡ Optimized
- **WebP Asset Migration:** Converted all banners, splash screens, and application icons to WebP. Reduced APK binary footprint by nearly 50% from 37 MB down to **20.3 MB**.
- **Repository Centralization:** Standalone monorepo `mikes-420grindhouse-app` for unified releases, in-app updates, and issue tracking.
- **UpdateManager:** Pointed native in-app update endpoints directly to the GitHub release feed.

---

## [v1.6.4] - Build 32 (2026-08-20)
### 💬 Added
- **Chat Account & Guest Access:** Persistent user credentials storage (`Settings > Chat Account`), automated login on startup and network reconnects, plus passwordless guest mode.
- **Fullscreen Chat Mode:** New dedicated action in the mobile/tablet navigation bar.
### 🛠️ Fixed
- **Mobile Responsive Layout:** Polished viewports and overlays for portrait and landscape orientations (slim margins, responsive playlist queue).
- **Flavored In-App Updates:** Full Edition downloads `.full.apk`, Light Edition downloads TV-optimized release.

---

## [v1.6.3] - Build 31 (2026-08-19)
### 🛠️ Fixed & Improved
- **Touch & Tablet Navigation:** Hid TV D-Pad visual prompts on touchscreen devices.
- **Movie Details & Trivia:** New dedicated trivia button in the mobile action bar.
- **Auto-Hide & YouTube Play/Mute:** Improved watchdog stability during player rebuilds and stream transitions.

---

## [v1.6.2] - Build 30 (2026-08-19)
### 📺 Added
- **CyTube Live Media Sync:** Drift correction and real-time Play/Pause synchronization with the channel.
- **Signing:** Release APKs now signed with standard v2+v3 signature schemes.

---

## [v1.6.1] - Build 29 (2026-08-19)
### 🎨 Visuals
- **16:9 TV Banner & App Icons:** Real 16:9 Leanback banners in 4 resolutions and custom Grindhouse spiral launcher icons.

---

## [v1.6.0] - Build 28 (2026-08-19)
### 🎬 Features
- **Live Progress & Spectator Count:** Real-time WebSocket status bar showing channel viewers and playback progress.
- **Up-Next Queue:** Preview of the next three upcoming titles in the bottom bar.
- **Typography & TV Safe Zones:** Refined typography and 5% overscan safety margins for televisions.

---

## [v1.5.0] - Build 27 (2026-08-19)
### 🐛 Features
- **1-Click In-App Bug Reporter:** Report issues directly from settings (automatically attaches device model, Android OS version, and active media title).

---

## [v1.4.0] - Build 26 (2026-08-19)
### 🎨 Themes & Parsers
- **4 OLED TV Themes:** *The Cinematic Deep*, *Premium Cyber Punk*, *Mystic Editorial*, and *Grindhouse Original*.
- **Series & Episode Detection:** Automatic regex parsing of season and episode numbers from YouTube titles.
