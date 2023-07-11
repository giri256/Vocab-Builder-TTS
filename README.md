# Vocab Builder TTS

Vocab Builder TTS is an interactive GUI tool designed to enhance your vocabulary learning experience. It takes a list of words as input, fetches their definitions, and generates Text-to-Speech (TTS) audio. Very useful to make custom audio-books of your difficult words for the exams like GRE, IELTS, TOEFL. So that you can listen to that on-fly while carrying on with your daily activities

![image](https://github.com/giri256/Vocab-Builder-TTS/assets/80974392/1b7440d6-75a1-4bd2-9066-9928b9cf1206)


## Prerequisites

Before getting started, you'll need to set up the following:

- **Word Information**: Make an account with either OpenAI or Merriam-Webster Dictionary. 
  - **OpenAI**: Register at [OpenAI](https://platform.openai.com/signup/). Once you have your API key, the tool can use the GPT-3.5 model to provide comprehensive word definitions, memorization tips, and example sentences.
  - **Merriam-Webster Dictionary**: Register at [Merriam-Webster Dictionary](https://dictionaryapi.com/register/index). With your API key, the tool fetches word definitions and example sentences from the dictionary.

- **Text-to-Speech (TTS) Audio**: Making an account with ElevenLabs is optional but recommended for better quality audio. Register at [ElevenLabs](https://beta.elevenlabs.io/sign-up) to get your API key. If you prefer not to incur any cost, the tool can use a local TTS engine, Tacotron2 from SpeechBrain, which generates audio using pre-trained models.

## Features

- **Flexible Word Information Retrieval**: The tool provides two options for fetching word information:
  - **GPT-3 Model**: This option uses the GPT-3.5 model from OpenAI to provide comprehensive word definitions, memorization tips, and example sentences.
  - **Merriam-Webster Dictionary**: This option fetches word definitions and example sentences from the Merriam-Webster Dictionary. This option provides straightforward definitions if you prefer a concise explanation.

- **Text-to-Speech (TTS) Audio Generation**: The tool generates TTS audio for each word and its information. It provides two options for generating the audio:
  - **Tacotron2 Model**: This is a local TTS engine from SpeechBrain that generates audio using the Tacotron2 and HIFIGAN models. It does not incur any cost as it downloads a few pre-trained models locally.
  - **ElevenLabs API**: This option uses the ElevenLabs API to generate high-quality TTS audio. Please note that this option may incur additional costs.

- **Audio Merging**: The tool provides an option to merge all the generated audio files into a single MP3 file for convenient listening. This currently works only if Tactoron2 model is selected, for Elevenlabs i am planning to implement this later

## How to Use

1. Ensure that you're running Python 3.11 or later.
2. git clone this repository : `git clone https://github.com/giri256/Vocab-Builder-TTS.git`
3. Install the required libraries by running `pip install -r requirements.txt`.
4. Run the script in any Python environment of your choice (e.g., Visual Studio Code).
5. Provide a list of words.
6. Choose the word information source (GPT-3 model or Merriam-Webster Dictionary).
7. Choose the TTS option (Tacotron2 or ElevenLabs).
8. The script will fetch the word information and generate TTS audio for each word.
9. The script will output an mp3 file in the same directory, which you can later import into your spotify library to listen on the go

**Note**: The Tacotron2 option requires the initial download of pre-trained models. While it can run on a CPU, using a GPU is recommended for faster performance.

## Credits

This project was made possible thanks to the following resources:

- [ElevenLabsLib](https://github.com/lugia19/elevenlabslib) for easy API access to ElevenLabs.
- The [Merriam-Webster Dictionary API](https://dictionaryapi.com/) for free use for non-commercial purposes.
