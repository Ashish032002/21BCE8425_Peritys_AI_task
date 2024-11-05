# 🔊 ULCA Audio Conversion Project

This project is a Python-based application that converts WAV audio files to FLAC format using the VITS (Variational Iterative Text-to-Speech) model. The application provides a web server interface that allows users to upload WAV files and receive the converted FLAC files.

## 🚀 Features

- Converts WAV audio files to FLAC format using the VITS model
- Provides a web server interface for file conversion
- Supports asynchronous processing of audio file conversion

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ulca-audio-conversion.git
   ```

2. Install the required dependencies:
   ```bash
   cd ulca-audio-conversion
   pip install -r requirements.txt
   ```

3. Download the pre-trained VITS model:
   ```bash
   git clone https://github.com/jaywalnut310/vits.git /content/vits_model
   ```

4. Run the application:
   ```bash
   python ulca.py
   ```
   The server will start running on `http://localhost:8080`.

## 🌐 Usage

1. Send a POST request to `http://localhost:8080/convert` with a `wav_file` field containing the WAV file you want to convert.
2. The server will process the WAV file, convert it to FLAC format, and return the FLAC file in the response.

## 📡 WebSocket Support

The project also includes a WebSocket interface for streaming audio conversion. To use the WebSocket interface, connect to `ws://localhost:8080/stream` and send the WAV file data over the WebSocket connection. The server will respond with the converted FLAC audio data.

## 🔍 Dependencies

- Python 3.7+
- PyTorch
- TorchAudio
- Librosa
- aiohttp
- websockets

🏗️ Program Structure
sample_data/
  dataset/
    test/
    train/
    val/
  data.json
  params.json
  README.md
  anscombe.json
  california_housing_test.csv
  california_housing_train.csv
  mnist_test.csv
  mnist_train_small.csv
vits_model/
  configs/
    ljs_base.json
    ljs_nosdp.json
    vctk_base.json
  filelists/
    ljs_audio_text_test_filelist.txt
    ljs_audio_text_train_filelist.txt
    ljs_audio_text_val_filelist.txt
    ljs_audio_text_val_filelist.txt
monotonic_align/
  __init__.py
  core.py
  setup.py
  resources/
  text/
  LICENSE
  README.md
  attentions.py
  commons.py
  data_utils.py
  inference.ipynb
  losses.py
  mel_processing.py
  models.py
  modules.py
  preprocess.py
  requirements.txt
  train.py
  train_ms.py
  transforms.py
  utils.py
