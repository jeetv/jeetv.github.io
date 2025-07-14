---
layout: page
title: Youtube Video Summarizer
description: 
img: assets/img/yt.png
importance: 1
category: fun
---

# [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/184_5JYhA-znu4y_UBbAFz-ioCVNkr9ZJ#scrollTo=rSOKwtbZ-y0S)
```

                ┌─────────────────────────────┐
                │     YouTube Video URL       │
                └────────────┬────────────────┘
                             │
                 ▼ Download & Metadata Extraction
        ┌────────────────────────────────────────┐
        │     PytubeFix: Download Video & Audio  │
        │     + Extract Video Metadata (JSON)    │
        └────────────────────────────────────────┘
                             │
                 ▼ Transcript Extraction
┌──────────────────────────────────────────────────────────┐
│  Try: YouTube Transcript API                             │
│  Fallback: Whisper (OpenAI model, local transcription)   │
└──────────────────────────────────────────────────────────┘
                             │
                 ▼ Scene Detection & Keyframes
┌────────────────────────────────────────────────────────────┐
│  PySceneDetect: Scene boundaries                           │
│  Save:                                                     │
│    - 1 keyframe/scene (for captioning & OCR)               │
│    - 4 frames/scene (optional for detailed captioning)     │
│    - Scene clips (for future extensions)                   │
└────────────────────────────────────────────────────────────┘
                             │
                 ▼ Visual Cue Extraction
┌────────────────────────────────────────────────────────────┐
│  OCR (EasyOCR) on 1 keyframe per scene                     │
│  GIT Image Captioning (microsoft/git-base) on frames       |
│  SmolVLM2 based Video Captioning                           |
│  Output:                                                   │
│    {scene_id: {"video_caption": ..., "ocr": [...]}}        │
└────────────────────────────────────────────────────────────┘
                             │
                 ▼ LLM-based Summarization
┌────────────────────────────────────────────────────────────────────┐
│  Transformers Pipeline (meta-llama/Llama-3.2-3B-Instruct)          │
│  Input = transcript + visual cues + structured system prompt       │
│  Output = point-wise, emotionally-aware, visually grounded summary │
└────────────────────────────────────────────────────────────────────┘

```