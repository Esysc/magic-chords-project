# 🎸 Magic Chords

A web application for **chord detection** and **audio transcription**.

Upload an audio file or paste a YouTube / SoundCloud link, and get a complete musical breakdown — chords, tempo, time signature, key, and transcribed lyrics — then export it in a variety of formats.

> **Production site:** [magic-chords.dev](https://magic-chords.dev)

---

## ✨ Highlights

- 🎵 **Chord detection** — hybrid of audio-analysis models plus a music-theory scoring layer for musically coherent results
- 📝 **Smart transcription** — automatic instrumental detection so you get clean lyrics
- 🎹 **Interactive playback** — rolling chord display with real-time highlighting
- 📦 **Multiple export formats** — classical partition, iReal Pro, guitar & bass tabs, MIDI, MusicXML
- 🌍 **Multi-language support**
- 📚 **Local library & setlists** — save analyzed songs to folders and organize them into setlists
- ✏️ **Editable metadata** — adjust tempo, time signature, and key, and watch measure boundaries re-split live
- ⚡ **Real-time progress** — live progress updates with accurate time estimates
- 🐳 **Docker-ready** — CPU and GPU deployment options

---

## 🧠 How it works

The app combines several approaches:

- **Madmom** & **Basic Pitch** for low-level audio → note/chord analysis
- **Whisper** for lyrics and vocal transcription
- **Essentia** for fast, optimized key and chord validation
- A custom **music-theory scoring** layer that turns raw detections into a musically meaningful result

Processing runs server-side with live updates streamed over WebSockets, and the frontend is lightweight vanilla JavaScript with no build step.

---

## 🛠️ Tech stack

| Layer     | Technology                              |
| ----------|--------------------------------------- |
| Backend   | Python 3.11, FastAPI                  |
| ML models | Madmom, Basic Pitch, Whisper, Essentia  |
| Task queue| Celery                                  |
| Frontend  | Vanilla JS (no framework, no build step)|
| Storage   | Redis                                   |
| Deploy    | Docker / Docker Compose, Caddy          |

---

## 🗂️ Project Board

Track development progress, upcoming features, and task planning on our [GitHub Project Board](https://github.com/users/Esysc/projects/1).

---

If you'd like to reach out about the project, feel free to open an issue or a discussion.

---

*© Magic Chords. All rights reserved.*