# JUJU LipSync — downloads (beta)

AI-enhanced visual dubbing for original live-action performances: drop a commercial and its approved foreign-language dialogue, and JUJU LipSync re-times only the mouths the new language needs. The original photography stays the master.

**[Download the latest version](https://github.com/mikeparsonstv-rgb/JUJU-LipSync/releases/latest)**. Open the `.dmg` and drag JUJU LipSync to Applications.

## Requirements

- An Apple silicon Mac with macOS 26 or later.
- At least 32 GB of memory. 64 GB or more is recommended.
- About 25 GB of free disk space for the on-device engine.
- [Homebrew](https://brew.sh). The engine uses ffmpeg and eSpeak NG, and the app installs them through Homebrew if they aren't there yet.

## First launch: setting up the engine

JUJU LipSync renders entirely on your Mac. The first time it opens, it offers to build its engine. The engine is built from its original sources, exactly as tested:

- **TBDub's code** (Apache-2.0), from GitHub, at the reviewed commit.
- **Model weights**, from Hugging Face and their publishers, at pinned revisions. That is about 15 GB.
- **Python and its packages**, each pinned by version and checksum. That is about 4 GB.

Every file is checked against its SHA-256 checksum before it is used. The install takes about 20 GB in all and can run for an hour on a slower connection. If it stops, it carries on where it left off.

## Privacy

Nothing leaves your Mac. Pictures and audio are processed on this Mac only, and the app collects no data. The app makes network requests in only two cases:

- **During engine setup**, to download the engine.
- **The daily update check** against `appcast.xml` in this repository.

## Updates

Updates install from inside the app, from **JUJU LipSync → Check for Updates…**. The app also checks once a day. Each version is signed with Developer ID and notarised by Apple.

## Beta testers

This is a beta for invited testers. If a render doesn't look right, please send the shot's PDF report, the run's `logs` folder, and a note of what you expected.

## Third-party components

TBDub (Apache-2.0) runs with a documented Apple-GPU patch; the patch notes are listed in the app's engine folder. The other components are:

- Wan2.2 VAE (Apache-2.0)
- HuBERT (Apache-2.0)
- MediaPipe Face Landmarker (Apache-2.0)
- SpeechBrain ECAPA (Apache-2.0)
- OpenCV YuNet and SFace (Apache-2.0)
- wav2vec2-espeak-ctc (Apache-2.0)
- mlx-video VAE port (MIT)
- MLX (MIT)
- PyTorch (BSD)

ffmpeg and eSpeak NG are separate tools, installed by Homebrew under their own licences.

© 2026 JUJU VFX. All rights reserved.
