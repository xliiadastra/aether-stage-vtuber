# 04 — QA Verification Matrix & Next-Gen Evolution Roadmap (`AETHER-VTUBE 24/7`)

## 1. Automated Verification & Self-Healing QA Matrix
| Test Suite / Check | Target Component | Verification Criteria | Status |
|---|---|---|---|
| **12+ ArtMesh Layer Integrity** | `live2d_rig_engine.py` | Verifies all required layers (`ArtMesh_HairBack` .. `ArtMesh_AccessoryHalo`), valid SVG markup, and base64 RGBA PNG swatches | **PASS** |
| **Cubism 4/5 Spec Compliance** | `.model3.json`, `.cdi3.json`, `.physics3.json` | Verifies `Version: 3`, `EyeBlink` & `LipSync` parameter groups, and 4-chain harmonic pendulum `PhysicsSettings` | **PASS** |
| **Self-Healing Ban-Guard Loop** | `app.py` (`/api/superchat/process`) | Verifies prompt-injection & PII doxxing bait fails Attempt #1 and auto-heals on Attempt #2 with `safety_score >= 95` and `entertainment_dopamine_score >= 90` | **PASS** |
| **60FPS Viseme Lip-Sync & WAV** | `_synthesize_voice_and_visemes` | Verifies playable RIFF WAV header + 60FPS `A/I/U/E/O` viseme envelope (`ParamMouthOpenY`, `ParamMouthForm`) | **PASS** |
| **$100+ Red SuperChat Encore** | `generate_lyria_concert_performance` | Verifies `lyria-3.5` 30-second live singing trigger, chorus lyrics, and playable concert audio | **PASS** |
| **HITL Producer Safety Gate** | `/api/hitl/propose` & `/api/hitl/decide` | Verifies high-risk mutations pause in `PENDING_APPROVAL` and transition cleanly on `APPROVE` / `REJECT` | **PASS** |

---

## 2. Next-Generation Evolution Roadmap
1. **Direct VTube Studio WebSocket Plugin Bridge (`ws://localhost:8001`)**: Stream `ParamAngleX/Y/Z`, `ParamMouthOpenY`, and `ParamMouthForm` directly into desktop VTube Studio or OBS Browser Source at 60Hz.
2. **Multi-VTuber Dual-Host Collab Stage**: Run `Luna Cyber-Neko` and `K-Idol Nova` simultaneously in a conversational duet powered by `gemini-3.8-live` bidirectional audio streaming.
3. **Real-Time Gameplay Screen Capture Commentary**: Feed live 1FPS gameplay frames into `gemini-3.8-live` so the VTuber reacts to boss fights while reading SuperChats.
