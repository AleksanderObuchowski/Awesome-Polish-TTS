# Awesome-Polish-TTS
<img width="2848" height="1600" alt="image" src="https://github.com/user-attachments/assets/6fdbf9aa-f4f0-467c-b791-aebe44a6b61a" />

This repository focuses on resources that are directly useful for building, running, training, or evaluating TTS systems for the Polish language.

## Contents

- [Engines](#engines)
- [Voices](#voices)
- [Datasets](#datasets)
- [Training & Finetuning](#training--finetuning)
- [Text Processing](#text-processing)
- [Evaluation](#evaluation)
- [Embedded & Edge](#embedded--edge)
- [Apps & Integrations](#apps--integrations)
- [Commercial Use Notes](#commercial-use-notes)
- [Contributing](#contributing)
- [License](#license)

## TTS Models

- [Coqui XTTS v2](https://huggingface.co/coqui/XTTS-v2) — Multilingual TTS model supporting 17 languages including Polish, with zero-shot voice cloning, speaker interpolation, and strong prosody. One of the most proven open-source choices for Polish speech synthesis.
- [VoxPolska-Auralis](https://huggingface.co/salihfurkaan/VoxPolska-Auralis) — Dedicated Polish TTS model (1B params) fine-tuned from Llasa/Llama-3.2-1B, trained on 24,000+ Polish transcript–audio pairs. Produces clear 16 kHz audio with natural-sounding Polish speech.
- [OuteTTS 1.0-1B](https://huggingface.co/OuteAI/Llama-OuteTTS-1.0-1B) — LLM-based multilingual TTS (1B params) trained on ~60,000 hours of audio, with Polish listed as a supported language. Offers zero-shot voice cloning and native Polish text support without romanization.
- [Piper](https://github.com/rhasspy/piper) — Fast local neural TTS system with Polish `pl_PL` voices, making it one of the most practical offline choices for Polish TTS. Lightweight and well-suited for edge and home-assistant deployments.
- [MMS TTS Polish](https://huggingface.co/facebook/mms-tts-pol) — Polish checkpoint from Meta’s Massively Multilingual Speech project, using the VITS architecture. Available via Hugging Face Transformers (v4.33+), licensed CC-BY-NC 4.0.
- [RHVoice natan-pol](https://github.com/RHVoice/natan-pol) — Dedicated Polish voice for RHVoice, useful for accessibility-oriented and offline speech setups.

## Datasets

- [MC Speech Dataset](https://github.com/czyzi0/the-mc-speech-dataset) — Public-domain single-speaker Polish dataset with 24,018 short clips, transcripts for every clip, and more than 22 hours of audio, which makes it a strong starting point for single-speaker TTS experiments.
- [CML-TTS Polish](https://www.openslr.org/146/) — Polish subset of the multilingual CML-TTS corpus, distributed via OpenSLR under CC-BY 4.0, built from LibriVox audiobooks at 24 kHz. 
- [SpokesBiz](https://arxiv.org/pdf/2312.12364.pdf) — Open corpus of conversational Polish with over 650 hours of recordings, diarization, and manual punctuation and casing annotation; it is more conversational than classic studio TTS corpora and can be useful for data mining or style diversification. [web:11][web:163]
- [ParlaSpeech-PL 1.0](https://www.clarin.si/repository/xmlui/handle/11356/1686?show=full) — Parliamentary spoken corpus of Polish with 535,465 entries and about 1,010 hours of audio, plus word-level alignments and speaker metadata, licensed under CC BY-SA 4.0.
- [Polish Read Speech Corpus for Speech Tools and Services](http://arxiv.org/pdf/1706.00245.pdf) — High-quality studio Polish speech corpus released under an open license as part of the CLARIN speech-tools effort, intended to support text-to-phoneme conversion, alignment, diarization, and speech technology development. [web:14]
- [nEMO](https://github.com/amu-cai/nEMO) — Emotional Polish speech dataset with over 3 hours of recordings from nine actors portraying six emotions, with transcriptions and explicit usefulness for emotionally expressive TTS. 
- [YodaLingua-Polish](https://huggingface.co/datasets/Thomcles/YodaLingua-Polish) — Large Polish speech dataset described as TTS-ready, with 329,740 audio–transcription pairs, 893 hours, 11,357 speakers, 24 kHz audio, and permissive commercial-use-friendly licensing. 
- [Speech Wikimedia](https://arxiv.org/pdf/2308.15710.pdf) — Multilingual CC-BY-SA speech corpus covering 77 languages, including Polish, which may be useful for mining additional aligned Polish speech segments.

## Training & Finetuning

- [polish-tts-model-training](https://github.com/Comtegra/polish-tts-model-training) — Repository dedicated to ongoing experiments in training and fine-tuning Polish TTS models, with an explicit focus on assembling Polish datasets and testing model quality.
- [facebook/mms-tts-pol](https://huggingface.co/facebook/mms-tts-pol) — Ready Polish TTS checkpoint that can serve as a baseline model for inference, adaptation, or comparison against your own fine-tuned systems. 
- [CML-TTS / YourTTS paper](https://arxiv.org/abs/2306.10097) — The CML-TTS work released a multilingual TTS dataset including Polish and trained a multilingual YourTTS model on top of it, which makes it a useful paper-and-data reference for Polish-capable multilingual training setups.
- [PL-BERT](https://github.com/yl4579/PL-BERT) — Phoneme-level BERT model proposed for improving TTS prosody via phoneme modeling and grapheme prediction, useful as a research component in modern speech-synthesis pipelines.

## Text Processing

- [TransFon](https://www.mdpi.com/2076-3417/12/5/2758) — Rule-based grapheme-to-phoneme conversion system for Polish, created specifically to convert Polish orthography into phonemic transcription and useful for pronunciation modeling and lexicon work.
- [multilingual-g2p](https://github.com/jcsilva/multilingual-g2p) — Grapheme-to-phoneme toolkit based on eSpeak with explicit support for Polish `pl`, useful when you need a lightweight practical G2P component.
- [Polish Read Speech Corpus tools](http://arxiv.org/pdf/1706.00245.pdf) — The CLARIN Polish speech-tools project includes resources around text-to-phoneme conversion and speech-text alignment, which are directly relevant to preprocessing Polish TTS data. 
- [WikiPron / multilingual G2P research](https://www.aclweb.org/anthology/P16-1038.pdf) — Broad multilingual pronunciation resources can help bootstrap Polish lexicons and fallback pronunciation systems, especially when project-specific Polish dictionaries are incomplete.

## Evaluation

- [BIGOS](https://annals-csis.org/proceedings/2023/drp/pdf/1609.pdf) — Benchmark Intended Grouping of Open Speech corpora for Polish, created as an evaluation benchmark over open Polish speech datasets and useful when you want a more reproducible way to compare systems.
- [ParlaSpeech-PL](https://clarinsi.github.io/parlaspeech/) — Large aligned corpus with rich metadata that is useful for stress-testing pronunciation, robustness, and speaker diversity, even though it was not created purely as a TTS corpus.
- [nEMO](https://github.com/amu-cai/nEMO) — Good reference set for emotional expressiveness because it explicitly covers anger, fear, happiness, sadness, surprise, and neutral speech in Polish. 
- [MC Speech Dataset](https://github.com/czyzi0/the-mc-speech-dataset) — Useful baseline dataset for single-speaker intelligibility and naturalness comparisons because it is clean, transcribed, and public domain. 

## Embedded & Edge

- [microlena](https://github.com/ethanak/microlena) — Polish-language TTS system for microcontrollers using Mbrola as the speech synthesis engine, aimed at very constrained environments.
- [ESP32Gadacz](https://github.com/ethanak/ESP32Gadacz) — Simple Polish TTS library for ESP32, useful for offline embedded prototypes and device-side voice output.
- [Piper](https://github.com/rhasspy/piper) — In addition to desktop use, Piper is often attractive for edge deployment because it is local, fast, and designed for practical inference.

## Apps & Integrations

- [PyTDM](https://github.com/ggegoge/PyTDM) — Python library focused on Polish text-to-speech, useful when you want a lightweight Polish-specific wrapper or integration layer in Python projects. 
- [RHVoice + natan-pol](https://github.com/RHVoice/natan-pol) — Good fit for screen-reader and accessibility-style deployments that prioritize offline use and system integration.
- [Piper-based local assistants](https://github.com/rhasspy/piper) — Practical option for local assistants, automation, and Home Assistant-style speech pipelines because it runs fully offline and already has Polish voices available.


## Contributing

Contributions are welcome, especially for:

- new Polish voices
- open datasets
- training recipes
- benchmarks

Please prefer primary sources, include license information whenever possible, and keep descriptions short and factual.
