# OCI Speech - Learning Notes

## Overview
This video introduces **OCI Speech**, a service that converts audio tracks into text. It explains how developers can use Oracle's models for transcription, its supported features, language options, performance capabilities, and additional functionalities like normalization, closed caption support, and profanity filtering.

## Key Concepts
- **Speech to Text**: Converts audio or video speech into text.
- **Acoustic Language Models**: Oracle’s prebuilt models used to provide accurate transcription.
- **Deep Learning**: Advanced techniques powering the transcription process.
- **Object Storage Processing**: Directly processes files stored in Oracle Object Storage.
- **Timestamped Transcriptions**: Provides time-aligned, grammatically accurate text.
- **Multi-language Support**: English, Spanish, and Portuguese (more in future).
- **Batching**: Submit multiple files in a single call.
- **Fast Processing**: Transcribes hours of audio in under 10 minutes.
- **Confidence Score**: Accuracy indicator per word and per transcription.
- **Normalization**: Adjusts text to resemble human writing (e.g., numbers, addresses).
- **Profanity Filtering**: Options to remove, mask, or tag profane words.
- **SRT File Support**: Generates closed captions for video.

## Detailed Notes
- **Core Functionality**:
  - **OCI Speech** locks the data in audio tracks by converting speech to text.
  - Developers leverage Oracle’s **time-tested acoustic language models**.
  - No data science expertise is required.
  - **Transcriptions** are timestamped and grammatically accurate.

- **Processing**:
  - Uses **deep learning techniques** for transcription.
  - Processes data directly in **object storage**.
  - Can handle **multiple languages**: English, Spanish, and Portuguese.
  - **Batching support**: Multiple files submitted in one request.
  - **Speed**: Can transcribe hours of audio in less than 10 minutes.
  - Achieves this speed by **chunking audio into smaller segments**, transcribing each, then combining results into one file.

- **Output Quality**:
  - Provides **confidence scores** per word and per overall transcription.
  - Adds **punctuation** for readability and smoother downstream text processing.

- **Additional Features**:
  - **SRT File Support**:
    - Most popular closed caption format.
    - Enables adding captions to videos.
  - **Normalization**:
    - Makes transcribed text resemble natural human writing.
    - Normalizes items like **addresses, times, numbers, URLs**.
    - Example: literal transcription on the left vs normalized with numbers converted into numeric symbols on the right.
  - **Profanity Filtering**:
    - **Remove**: replaces with asterisks.
    - **Mask**: retains the first letter, replaces the rest with asterisks.
    - **Tag**: keeps the word but marks it in the output data.

## Important Terms
- **OCI Speech**: Oracle Cloud service for speech-to-text transcription.
- **Acoustic Language Models**: Prebuilt models enabling accurate transcription.
- **Deep Learning**: Technique used for high-accuracy automatic transcription.
- **Object Storage**: Location where files are processed directly.
- **Timestamped Transcription**: Text aligned with audio timing.
- **Batching**: Submitting multiple files for transcription in one request.
- **SRT File**: Standard closed caption format.
- **Normalization**: Adjusting transcribed text into natural, human-readable form.
- **Profanity Filtering**: Options to remove, mask, or tag profanity in text output.

## Summary
OCI Speech is a **straightforward speech-to-text service** that uses Oracle’s models and deep learning to provide accurate, timestamped, and normalized transcriptions. It supports multiple languages, batching, and fast processing by chunking audio. The service enhances usability with **confidence scores, punctuation, SRT support, normalization, and profanity filtering**, making it a comprehensive tool for developers needing high-quality transcriptions.
