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

project/
├── sample_data/                     # Main data directory
│   ├── dataset/                     # Organized dataset folders
│   │   ├── test/                   # Test dataset
│   │   ├── train/                  # Training dataset
│   │   └── val/                    # Validation dataset
│   ├── data.json                   # General data configuration
│   ├── params.json                 # Parameter settings
│   ├── README.md                   # Data documentation
│   ├── anscombe.json              # Anscombe dataset
│   ├── california_housing_test.csv  # California housing test data
│   ├── california_housing_train.csv # California housing training data
│   ├── mnist_test.csv             # MNIST test dataset
│   └── mnist_train_small.csv      # MNIST training subset
│
├── vits_model/                     # VITS model directory
│   ├── configs/                    # Configuration files
│   │   ├── ljs_base.json          # LJSpeech base config
│   │   ├── ljs_nosdp.json         # LJSpeech no-SDP config
│   │   └── vctk_base.json         # VCTK base config
│   └── filelists/                 # Audio-text filelists
│       ├── ljs_audio_text_test_filelist.txt
│       ├── ljs_audio_text_train_filelist.txt
│       └── ljs_audio_text_val_filelist.txt
│
└── monotonic_align/               # Monotonic alignment module
    ├── resources/                 # Resource files
    ├── text/                      # Text processing files
    ├── __init__.py               # Package initializer
    ├── core.py                   # Core functionality
    ├── setup.py                  # Setup configuration
    ├── LICENSE                   # License file
    ├── README.md                 # Documentation
    ├── attentions.py            # Attention mechanisms
    ├── commons.py               # Common utilities
    ├── data_utils.py            # Data utilities
    ├── inference.ipynb          # Inference notebook
    ├── losses.py                # Loss functions
    ├── mel_processing.py        # Mel spectrogram processing
    ├── models.py                # Model definitions
    ├── modules.py               # Module implementations
    ├── preprocess.py            # Data preprocessing
    ├── requirements.txt         # Dependencies
    ├── train.py                # Training script
    ├── train_ms.py             # Multi-speaker training
    ├── transforms.py           # Data transformations
    └── utils.py                # Utility functions



