# Mind Rhythm Sampler
> For the "I have a rhythm in my mind but can't play keys" producer

Voice-first → Mind-first architecture. Your edge is massive: Dubler proved $300+ WTP for voice-to-MIDI. This is voice → intent + timbre.

## The Insight
Producers beatbox ideas into voice memos. Keys are the bottleneck. Capture the rhythm you hear in your head without playing keys.

## Architecture (see diagram artifact)
- **Input Layer**
  - Voice Mode (TODAY): Hum, Beatbox, Whistle → <20ms Web Audio API
  - Mind Mode (NEXT): Imagined Rhythm, EEG Alpha (Muse 2 / OpenBCI / Emotiv)
- **AI Brain** [DETECTION → UNDERSTANDING → GENERATION]
  - Detection: Basic Pitch / CREPE / librosa onset
  - Understanding: Quantizer + Intent (trap? lo-fi? bossa?) swing preservation
  - Generation: RAVE / DDSP / MusicGen / Stable Audio
- **Sampler Station**: 16-pad MPC mapping (puh=Kick, tss=Hat), MIDI/WAV/VST/Ableton Link, Style Transfer "Make it sound like..."

## Tech Stack
- Frontend: Next.js + Tone.js + WebAssembly (Basic Pitch WASM)
- Backend: Python FastAPI + PyTorch + ONNX + WebSockets
- Audio: JUCE for VST3/AU, WebAudio fallback, Ableton Link
- Models: Basic Pitch, RAVE, MusicGen Small, Stable Audio

## Roadmap
- Phase 1 (1 month) — Voice MVP: Web beatbox → MIDI, quantizer, pads, export
- Phase 2 (2-3) — Style Transfer: RAVE timbre, prompts like "Dilla loose"
- Phase 3 (4-6) — EEG Rhythm: Muse 2 alpha, imagined tap classification
- Phase 4 (6+) — Full Station: Hardware concept + community kits

## Why win vs Dubler 2
Dubler maps voice → MIDI note. We map voice → intent + timbre. Quantizer keeps human feel, RAVE keeps breath envelope.

Built for producers who have rhythm in mind but can't play keys. ♡
