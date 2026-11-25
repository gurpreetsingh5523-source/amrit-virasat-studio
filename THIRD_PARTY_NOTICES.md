# Third-party notices

Amrit Virasat Studio's own code is under the PolyForm Noncommercial License 1.0.0 (see `LICENSE` and
`NOTICE`). It uses the software below, which keeps its own license. Nothing here is bundled into the
repository except the Mukta Mahee font; everything else is installed by `setup.sh` or by you.

Licenses were read from each package's metadata in October 2026. This is a summary, not legal advice.

## Installed by `setup.sh` (permissive or LGPL — compatible with the Studio's license)

| Package | Used for | License |
|---|---|---|
| PySide6 (Qt for Python) | the whole user interface | LGPL-3.0 |
| pygame | Sequencer playback | LGPL-2.1 |
| numpy, scipy, scikit-learn, numba | audio maths | BSD |
| librosa | audio analysis | ISC |
| soundfile, soxr | reading/writing audio, resampling | BSD-3-Clause / LGPL-2.1 |
| sounddevice | microphone and live playback | MIT |
| pyloudnorm | loudness (LUFS) | MIT |
| mido, python-rtmidi | MIDI | MIT |
| noisereduce | noise reduction (second method) | MIT |
| faster-whisper, ctranslate2 | speech → text | MIT |
| pdfplumber | reading PDFs | MIT |
| pydub | audio conversion | MIT |
| pillow | images, video frames, cover art | MIT-CMU (HPND) |
| keyring | storing your API keys in the macOS Keychain | MIT |
| python-pptx, lxml | 📓 Notebook → PowerPoint (.pptx) | MIT, BSD-3-Clause |
| XlsxWriter | 📓 Notebook → Excel (.xlsx) | BSD-2-Clause |
| SpeechRecognition | speech input | BSD |
| requests | web requests | Apache-2.0 |

## External tools (installed with Homebrew, run as separate programs)

| Tool | Used for | License |
|---|---|---|
| ffmpeg | every audio/video conversion | LGPL-2.1+ (Homebrew builds may include GPL parts) |
| yt-dlp | downloading from links | Unlicense |
| deno | needed by yt-dlp for YouTube | MIT |

## Optional — GPL-3.0 (NOT installed by default)

These are GPL-3.0. The Studio works fully without them; install them yourself only if you want what they add.

| Package | What it adds | Without it |
|---|---|---|
| pedalboard (Spotify) | hosting your own VST3 / Audio Unit plugins in ⚙️ Pro Engine | the Studio's own effects (`engines/music/builtin_fx.py`) are used |
| edge-tts | Microsoft Edge online voices | other voices (Google, MMS, OmniVoice, Gemini, …) |

Also optional and **AGPL-3.0**: **PyMuPDF** (`fitz`). If it is installed, the 📓 Notebook uses it to read PDFs
(faster); without it, pdfplumber (MIT, installed by `setup.sh`) is used. Not installed by `setup.sh`.

The 📓 Notebook's "🔎 Discover" searches **Wikipedia** through its public API; article text is CC BY-SA —
keep the article link (the Notebook stores it with the source) when you share what you made from it.

## AI models (downloaded on first use, never stored in this repository)

Each model has its own license and terms. Check the model card before any commercial use.

| Model | Used for | Where it comes from |
|---|---|---|
| BS-Roformer / Mel-Roformer (via `audio-separator`) | 🎙 Voice Rescue: best voice separation, AI denoise, de-reverb | UVR model repository (via python-audio-separator, MIT) |
| Demucs (htdemucs) | 📥 Stems AI separation | Meta (MIT) |
| Whisper (via faster-whisper) | speech → text | OpenAI (MIT) |
| IndicConformer | Punjabi speech → text | AI4Bharat (gated on Hugging Face) |
| DeepFilterNet | speech noise removal | Rikorose/DeepFilterNet |
| IndicF5, OmniVoice, MMS | Punjabi voices | see each model card |

Cloud model plug-ins (Gemini, Veo, Nano Banana, OpenAI and others) are only used if **you** add your own
API key in ⚙️ Settings; their terms are between you and that provider.

## Font

**Mukta Mahee** (Gurmukhi) — © Ek Type, SIL Open Font License 1.1. The license is in `assets/fonts/OFL.txt`.
