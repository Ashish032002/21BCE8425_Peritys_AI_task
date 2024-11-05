# Project Structure

This repository contains a machine learning project with the following structure:

## Directory Structure

```
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
```

## Project Components

### 1. sample_data/
Contains all the datasets and their configurations:
- Organized dataset splits (train/test/val)
- Configuration files (data.json, params.json)
- Various datasets including California Housing and MNIST
- Dataset-specific documentation

### 2. vits_model/
Houses the VITS (Voice Text-to-Speech) model configurations:
- Different configuration JSONs for LJSpeech and VCTK
- Audio-text filelists for training, testing, and validation

### 3. monotonic_align/
Contains the core implementation files:
- Core functionality modules
- Attention mechanisms and model definitions
- Training and preprocessing scripts
- Utility functions and data processing tools
- Documentation and license information

## Setup and Usage

To use this project:

1. Install the required dependencies:
```bash
pip install -r monotonic_align/requirements.txt
```

2. Prepare your data:
- Place your datasets in the appropriate folders under `sample_data/dataset/`
- Configure the model parameters in `sample_data/params.json`

3. Training:
- Use `train.py` for single-speaker training
- Use `train_ms.py` for multi-speaker training

4. Inference:
- Refer to `inference.ipynb` for example usage and inference

## License

See `monotonic_align/LICENSE` for license information.
