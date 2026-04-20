---
title: YouTube Downloader (yt-dlp CLI Menu)
status: killed
created: 2026-03-26
review-after: 2026-04-04
killed: 2026-04-04
tags: [tool, python, content-creation]
---

# YouTube Downloader

## Why

Long YouTube videos (12+ hours) often lack subtitles, which makes content extraction tools useless. The workaround: download the audio, import into DaVinci Resolve, use its AI speech-to-text to generate subtitles, then export .srt files for further content work.

Downloading audio-only saves massive disk space (~500 MB vs 10-20 GB for a 12-hour video).

## What

A small Python project with an interactive CLI menu. Paste a YouTube URL, answer a few questions, get your file.

## CLI Menu Flow

```
=== YouTube Downloader ===

1. Paste URL
2. Choose download type:
   [1] Audio only (MP3) — recommended for subtitle generation
   [2] Audio only (WAV) — higher quality, larger file
   [3] Video + Audio (MP4)
3. If video selected, choose quality:
   [1] 720p  (~3-5 GB for 12h)
   [2] 1080p (~10-15 GB for 12h)
   [3] 4K    (~20-40 GB for 12h)
   [4] Best available
4. Choose output folder (default: ./downloads/)
5. Show video title + estimated file size before confirming
6. Download with progress bar
```

## Additional CLI Features

- **Resume interrupted downloads** — if a large download fails halfway, pick up where it left off
- **List available formats** — show what formats/qualities YouTube actually offers for this video (not all videos have 4K)
- **Batch mode** — paste multiple URLs (one per line) and download them all
- **Filename cleaning** — auto-sanitize the video title for a clean filename (remove special characters, limit length)
- **Download history** — simple log of what was downloaded (date, title, URL, format) so you don't accidentally re-download
- **Metadata display** — before downloading, show: title, channel, duration, upload date — so you confirm it's the right video

## Tech Stack

- **Python 3.x**
- **yt-dlp** — core download engine (`pip install yt-dlp`)
- **ffmpeg** — for stream merging and audio extraction (binary, no install needed)
- No other dependencies required

## Project Structure

```
youtube-downloader/
├── downloader.py       # Main CLI script
├── requirements.txt    # yt-dlp
├── downloads/          # Default output folder
├── history.log         # Download history
└── README.md           # Setup instructions
```

## Setup Steps

1. Create new project folder at `D:\14 Vibe Coding Projects\CLaude Code\youtube-downloader\`
2. Set up Python virtual environment (`python -m venv venv`)
3. Install yt-dlp (`pip install yt-dlp`)
4. Ensure ffmpeg is available on PATH (already installed on this machine)
5. Build the CLI menu script
6. Test with a short video first, then the 12-hour target

## Usage

Run from terminal (Cursor / Claude Code):
```
python downloader.py
```

That's it. The menu guides you through the rest.
