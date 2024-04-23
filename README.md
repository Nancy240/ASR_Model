# Whisper-Hindi-ASR-model-IIT-Bombay-Internship

The Whisper Hindi ASR (Automatic Speech Recognition) model is powered by the KathBath dataset, a comprehensive repository of spoken Hindi samples. Trained using advanced deep learning techniques, Whisper excels at converting spoken Hindi into accurate text. Its neural network architecture enables it to decipher the nuances of the Hindi language, including regional accents and dialects, with remarkable efficiency and precision.

The KathBath dataset forms the cornerstone of Whisper's training, featuring a diverse array of speech samples from various regions and on different topics. This diversity ensures Whisper's adaptability across real-world scenarios, facilitating reliable performance in diverse contexts.

In addition to transcribing speech, ASR models like Whisper calculate the Word Error Rate (WER) to assess accuracy. Lower WER values signify superior performance by comparing the model's output with a reference transcription.

- Link: https://github.com/openai/whisper
- Link: https://github.com/AI4Bharat/vistaar
- Link: https://github.com/belambert/asr-evaluation
- Test Dataset Link: https://asr.iitm.ac.in/Gramvaani/NEW/GV_Eval_3h.tar.gz

      Hello,
      Are you still looking for the internship at IIT Bombay for the Machine Learning Profile?
      If Yes then Kindly do this task. we expect you to complete a short assignment that just takes one day. But we are providing 7 days to complete.  

      You must implement the Whisper Hindi (Automatic Speech Recognition) ASR model. Also calculate the WER for Kathbath dataset
      Just give us WER for the kathbath dataset.

      Thanking You
      Ayush
      IIT Bombay
## Word Error Rate(WER)


Word Error Rate (WER) serves as a crucial metric for evaluating automatic speech recognition (ASR) systems. It quantifies the discrepancy between the transcribed output produced by the ASR system and the reference transcription (ground truth). Here are the key points:

-Calculation: WER is computed by comparing the total number of errors (insertions, deletions, and substitutions) needed to align the ASR-generated text with the reference text. This count is then divided by the total number of words in the reference text.
-Accuracy Assessment: Lower WER values indicate higher accuracy. A perfect WER score of 0 signifies an exact match between the transcribed and reference texts.
-Comprehensive Evaluation: WER considers both misrecognitions (substituted or incorrect words) and omissions (missing words) in the transcription, providing a holistic view of ASR performance.
-Application: WER is widely used across various languages and contexts to assess ASR quality and guide improvements.
## Whisper Model

Whisper stands as a versatile speech recognition model designed for diverse applications. Trained on a vast array of audio data, it boasts multitasking capabilities, including multilingual speech recognition, speech translation, and language identification.

![approach](https://private-user-images.githubusercontent.com/120269805/324206437-ba812c1b-8e2e-404c-a0b2-f3aa39b453cc.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTM5MDgwMTgsIm5iZiI6MTcxMzkwNzcxOCwicGF0aCI6Ii8xMjAyNjk4MDUvMzI0MjA2NDM3LWJhODEyYzFiLThlMmUtNDA0Yy1hMGIyLWYzYWEzOWI0NTNjYy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDIzJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQyM1QyMTI4MzhaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNGIyMWU1Nzk3NTM2NDFiYWJiNDVhMGE5MDIxMDg0MDJkYjU5NjU0NGNmN2FkYTU2NjFjNjI5YTA0NTU5MzNhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.R4OHfVOWaPSI0RhP35CqLLJdLGJbS6tFiA-s955Qcfc)

At its core lies a Transformer sequence-to-sequence architecture, honed through training on various speech processing tasks. These tasks encompass multilingual speech recognition, speech translation, spoken language identification, and voice activity detection. Remarkably, Whisper consolidates these functions into a single model, supplanting multiple stages typically found in conventional speech processing pipelines.

This multitask training regimen is facilitated by a series of specialized tokens embedded within the model. These tokens act as task specifiers or aids for classification, streamlining the model's ability to tackle a broad spectrum of speech-related tasks efficiently.

## Setup

We used Python 3.9.9 and PyTorch 1.10.1 to train and test our models, but the codebase is expected to be compatible with Python 3.8-3.11 and recent PyTorch versions. The codebase also depends on a few Python packages, most notably OpenAI's tiktoken for their fast tokenizer implementation. You can download and install (or update to) the latest release of Whisper with the following command:

      pip install -U openai-whisper
Alternatively, the following command will pull and install the latest commit from this repository, along with its Python dependencies:

      pip install git+https://github.com/openai/whisper.git 
To update the package to the latest version of this repository, please run:

      pip install --upgrade --no-deps --force-reinstall git+https://github.com/openai/whisper.git
It also requires the command-line tool ffmpeg to be installed on your system, which is available from most package managers:

      #on Ubuntu or Debian
      sudo apt update && sudo apt install ffmpeg

      # on Arch Linux
      sudo pacman -S ffmpeg

      # on MacOS using Homebrew (https://brew.sh/)
      brew install ffmpeg

      # on Windows using Chocolatey (https://chocolatey.org/)
      choco install ffmpeg

      # on Windows using Scoop (https://scoop.sh/)
      scoop install ffmpeg
