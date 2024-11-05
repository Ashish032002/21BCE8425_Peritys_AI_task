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

## 💡 Future Improvements

- Add support for batch processing of multiple audio files
- Implement more efficient audio conversion algorithms
- Provide a web-based user interface for file conversion
- Add support for more audio file formats

## 📄 License

This project is licensed under the [MIT License](LICENSE).
