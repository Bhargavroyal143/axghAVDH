# CueDeck (Tauri v2)
Prereqs: Node 18+, Rust, platform deps (https://tauri.app/start/prerequisites/)

    npm install
    npm run tauri icon path/to/any-1024px.png   # icons generate chestundi
    npm run tauri dev

Mundu app lo Deepgram + Anthropic keys adugutundi (localStorage lo untayi).
Hotkey: Cmd+Enter (Mac) / Ctrl+Enter (Windows).
Meeting start chese mundu andariki consent teesukondi. Recording indicator always kanipistundi.

Phase 2 (done): Windows system audio via cpal WASAPI loopback -> "Them" channel, mic -> "You" channel (Deepgram multichannel).
macOS system audio (ScreenCaptureKit) = TODO; mac lo ippudu mic only.

## Installer build (no local Rust needed)
1. GitHub lo kotha repo create chesi ee folder anta upload cheyyandi.
2. Actions tab -> "Build CueDeck installers" -> Run workflow.
3. 10-15 min tarvata Releases (draft) lo Windows (.msi/.exe) + macOS (.dmg) vastayi.
Local: `npm run tauri build` -> src-tauri/target/release/bundle/
Installers unsigned: Windows SmartScreen / macOS Gatekeeper warning vastundi (More info -> Run anyway; Mac: right-click -> Open).

## Screenshot context
"📷 Screen" checkbox on chesthe, Assist/hotkey nappudu primary monitor screenshot (max 1280px) Claude ki pampabadutundi.
macOS: System Settings > Privacy > Screen Recording lo CueDeck ki permission ivvali.
Screen lo sensitive info (passwords, private chats) unte checkbox off cheyyandi.
