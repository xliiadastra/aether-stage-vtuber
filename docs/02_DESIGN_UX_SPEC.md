# 02 — Design System, 60FPS Stage & UX Specification (`AETHER-VTUBE 24/7`)

## 1. Broadcast Studio Tri-Pane Layout
The operator UI (`static/index.html`) is engineered as a zero-latency **Dark-Mode Broadcast Control Room**:
1. **Left Dock — Live2D Cubism 4/5 Rigging Factory**:
   - Instant archetype selector across **Luna Cyber-Neko**, **Seraphina Rune**, and **K-Idol Nova**.
   - Interactive **12+ Separated PSD/SVG/PNG ArtMesh Layer Tree** (`ArtMesh_HairBack` through `ArtMesh_AccessoryHalo`) with per-layer visibility toggles, vertex counts, and deformer parent bindings.
   - Live JSON tabbed inspector and one-click downloader for `.model3.json`, `.cdi3.json`, and `.physics3.json`.
2. **Center Stage — 60FPS Interactive Multi-Layer Live2D Puppet & Telemetry**:
   - Runs at a locked **60FPS (`requestAnimationFrame`)** driving hierarchical SVG deformer groups:
     - **Gaze & Head Rotation (`ParamAngleX`, `ParamAngleY`, `ParamAngleZ`)**: Blends smooth cursor tracking with autonomous idle breathing oscillation.
     - **Hooke/Verlet Pendulum Spring Solver**: Real-time secondary motion for `ParamHairFront`, `ParamHairSide`, `ParamHairBack`, and `ParamHaloFloat`.
     - **60FPS RMS Lip-Sync Viseme Driver (`A / I / U / E / O`)**: Synchronizes `ParamMouthOpenY` and `ParamMouthForm` with synthesized WAV audio and highlights active vowel viseme pills in real time.
     - **Emotion Motion Trigger Bar**: One-click or SuperChat-driven triggers (`star_eyes`, `blush_panic`, `savage_smirk`, `headbang_hype`, `idol_wink`).
3. **Right Dock — Multi-Platform SuperChat Console, Self-Healing Log & HITL Gate**:
   - Supports **YouTube SuperChat**, **Chzzk Cheese**, **Twitch Bits**, and **TikTok Gifts**.
   - Real-time **Self-Healing Broadcast Safety & Ban-Guard Audit Feed** displaying Attempt #1 (Blocked unsafe draft/bait) -> Attempt #2 (Self-healed witty in-character deflection).
   - **Mandatory HITL Safety Gate** cards with `BEFORE` / `AFTER` JSON diff inspection and `Approve` / `Reject` producer controls.
