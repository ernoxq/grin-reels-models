# GRIN Reels — speech model

This repo hosts the speech-recognition model that the **GRIN Reels** skill downloads when it runs in a Claude chat. Nothing here needs to be installed by hand.

## What's in release `v1`

| File | What it is |
|---|---|
| `config.json` | model settings |
| `model.bin` | model weights (~480 MB) |
| `tokenizer.json` | tokenizer |
| `vocabulary.txt` | vocabulary |

These files are an unmodified copy of [Systran/faster-whisper-small](https://huggingface.co/Systran/faster-whisper-small), the CTranslate2 conversion of OpenAI Whisper *small*. They are redistributed under the MIT License; see `LICENSE`.

## How the skill uses it

```
https://github.com/ernoxq/grin-reels-models/releases/download/v1/<file>
```

`autocut/fetch_model.py` downloads the four files once per chat into `~/.cache/grin-reels/whisper-small`.

---
GRIN Reels © 2026 Ernest Grin (GRIN studio). The GRIN Reels engine and skills are licensed separately and are **not** part of this repo.
