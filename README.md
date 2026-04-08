# Voice Deepfake Detector

Real-time audio deepfake detection system that distinguishes genuine
human speech from AI-generated or voice-cloned audio using deep learning
on mel spectrograms.


---

## The Problem

Voice cloning technology has advanced to the point where anyone can
clone a voice in seconds using tools like ElevenLabs, PlayHT, or
OpenAI Voice. This enables:

- **Phone fraud** — scammers impersonating family members or bank officials
- **Political disinformation** — fabricated audio of public figures
- **Identity theft** — bypassing voice-based authentication systems
- **Non-consensual impersonation** — cloning voices without consent

Human listeners can no longer reliably distinguish real from fake.
Automated detection is now essential infrastructure.

---

## The Solution

A deep learning classifier trained on mel spectrograms that captures
the subtle acoustic artifacts present in AI-generated speech but absent
in genuine human voice — micro-tremors, unnatural prosody, spectral
smoothness, and vocoder fingerprints.

---

## Pipeline

Audio file (.wav/.mp3)
↓
Preprocessing (resampling, normalization, silence removal)
↓
Mel Spectrogram extraction (128 mel bands, 25ms windows)
↓
CNN / Lightweight Transformer
↓
Real / Fake probability + confidence score
↓
Spectrogram visualization with anomaly highlighting
---

---

## Tech Stack

| Layer | Technology |
|---|---|
| Audio processing | librosa, soundfile |
| Feature extraction | Mel spectrograms, MFCCs, chroma |
| Deep learning | PyTorch |
| Model architecture | CNN + attention |
| Web interface | Flask |
| Dataset | ASVspoof 2019 |

---

## Project Structure

voice-deepfake-detector/
├── data/
│   └── (download instructions in docs/DATA.md)
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_extraction.ipynb
│   ├── 03_model_training.ipynb
│   └── 04_evaluation.ipynb
├── src/
│   ├── preprocessor.py
│   ├── features.py
│   └── model.py
├── app/
│   ├── app.py
│   └── templates/
├── outputs/
└── README.md

---

## Progress

- [x] Project defined and documented
- [ ] Dataset preparation
- [ ] Feature extraction pipeline
- [ ] Model training
- [ ] Evaluation and visualization
- [ ] Web interface

---

## Author

**Hidayet Allah Yaakoubi**
BME Student — Tunisia 🇹🇳
[GitHub](https://github.com/Hidaayet) ·
[Email](mailto:hideyayaakoubi16@gmail.com)