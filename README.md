# AETHER-VTUBE 24/7 — Autonomous Live2D Avatar Rigging & Zero-Latency SuperChat AI Streamer Studio

> **Service Port**: `8010`  
> **Google AI Stack**: `google-genai >= 2.30.1` (`gemini-4-argon`, `gemini-nano-banana-2.1`, `gemini-3.8-flash-tts`, `lyria-3.5`, `gemini-3.8-live`)

## Overview
**AETHER-VTUBE 24/7** is an end-to-end autonomous Live2D avatar rigging factory and 24/7 livestreaming studio:
1. **Automated Live2D Model & Cubism 4/5 Rigging Factory (`live2d_rig_engine.py`)**:
   - Generates **12+ separated PSD/SVG/PNG ArtMesh layers** (`ArtMesh_HairBack`, `ArtMesh_Body`, `ArtMesh_HeadBase`, `ArtMesh_EyeL`, `ArtMesh_EyeR`, `ArtMesh_PupilL`, `ArtMesh_PupilR`, `ArtMesh_BrowL`, `ArtMesh_BrowR`, `ArtMesh_Mouth`, `ArtMesh_HairSideL/R`, `ArtMesh_HairFront`, `ArtMesh_AccessoryHalo`).
   - Exports valid Live2D Cubism 4/5 `.model3.json`, `.cdi3.json`, and `.physics3.json` pendulum spring-physics bundles.
   - Includes 3 VTuber archetypes: **Luna Cyber-Neko**, **Seraphina Rune**, and **K-Idol Nova**.
2. **Self-Healing Broadcast Safety & Ban-Guard Verification Loop (`app.py`)**:
   - Inspects incoming donations across **YouTube SuperChat**, **Chzzk Cheese**, **Twitch Bits**, and **TikTok Gifts** using `gemini-4-argon`.
   - Automatically intercepts prompt injection, PII/doxxing, and ToS bait, rewriting the reply with witty in-character deflection until `safety_score >= 95` and `entertainment_dopamine_score >= 90`.
3. **60FPS RMS Viseme Lip-Sync (`gemini-3.8-flash-tts`) & $100+ Live Concert (`lyria-3.5`)**:
   - Synthesizes playable WAV speech + a 60FPS `A / I / U / E / O` viseme envelope (`ParamMouthOpenY`, `ParamMouthForm`) and emotion triggers (`star_eyes`, `blush_panic`, `savage_smirk`, `headbang_hype`, `idol_wink`).
   - Triggers a 30-second live singing performance via `lyria-3.5` whenever a `$100+` Red SuperChat drops.
4. **Mandatory HITL Broadcast Safety Gate**:
   - Pauses high-risk broadcast mutations (sponsor integrations, YouTube/Twitch title/category API updates, VIP donor ban-hammers) for explicit human `Approve` / `Reject` sign-off.

## Quickstart
```bash
uvicorn app:app --host 0.0.0.0 --port 8010
```
Run tests:
```bash
.venv/bin/pytest tests/test_app.py -v
```
