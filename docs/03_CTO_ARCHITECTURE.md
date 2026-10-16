# 03 — CTO System Architecture & Google GenAI SDK Patterns (`AETHER-VTUBE 24/7`)

## 1. End-to-End Architecture Diagram

```mermaid
flowchart TD
    subgraph RigFactory["Part 1: Live2D Cubism 4/5 Rigging Factory (live2d_rig_engine.py)"]
        NB["gemini-nano-banana-2.1\n(Character Sheet Texture)"] --> L12["12+ Separated PSD/SVG/PNG ArtMesh Layers"]
        ARG1["gemini-4-argon\n(Deformer & Spring Physics Calibration)"] --> CUB["Cubism 4/5 Bundle\n(.model3.json / .cdi3.json / .physics3.json)"]
    end

    subgraph StreamerLoop["Part 2: 24/7 Autonomous SuperChat Loop (app.py)"]
        SC["Incoming SuperChat / Chzzk Cheese / Twitch Bits / TikTok Gifts"] --> GUARD["gemini-4-argon\nSelf-Healing Broadcast Safety & Ban-Guard Loop"]
        GUARD -->|"safety < 95 or dopamine < 90"| HEAL["Auto-Rewrite Witty In-Character Deflection\n(previous_interaction_id)"]
        HEAL --> GUARD
        GUARD -->|"safety >= 95 & dopamine >= 90"| TTS["gemini-3.8-flash-tts\n+ 60FPS Viseme Envelope (A/I/U/E/O)"]
        SC -->|"$100+ Red SuperChat"| LYRIA["lyria-3.5\n30s Live Singing Encore Performance"]
    end

    subgraph StageUI["Part 3: 60FPS Live2D Stage & HITL Studio (static/index.html)"]
        CUB --> STAGE["60FPS Interactive SVG/Canvas Deformer Stage"]
        TTS --> STAGE
        LYRIA --> STAGE
        HITL["Mandatory HITL Safety Gate\n(Sponsor / Title Mutation / VIP Ban)"]
    end
```

---

## 2. Official `google-genai >= 2.30.1` Interactions API Compliance
Every model invocation strictly follows the Oct 2026 `google-genai >= 2.30.1` Interactions API (`client.interactions.create(...)`):
- **No legacy `generate_content`**: All text, structured JSON (`response_format`), image (`gemini-nano-banana-2.1`), audio (`gemini-3.8-flash-tts`), and music (`lyria-3.5`) calls use `client.interactions.create(...)` with plain dict `generation_config` and `thinking_level`.
- **Stateful Self-Healing Continuation**: When an adversarial donation fails Attempt #1 in the Broadcast Safety Loop, Attempt #2 chains state via `previous_interaction_id` to produce an in-character roast deflection that satisfies `safety_score >= 95` and `entertainment_dopamine_score >= 90`.
