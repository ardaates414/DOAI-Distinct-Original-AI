# DOAI-Distinct-Original-AI
The New Era Of Infinite Use Of AI
---------------------------------

# DOAI - Distinct Original AI

A custom AI desktop application with a sleek, Apple-inspired interface, built from scratch with PyTorch and PyQt6.

![DOAI Screenshot](screenshot.png)

## Features

- 🚀 **Modern, responsive UI** inspired by Apple design
- 💬 **Chat interface** for natural language interaction
- 🧠 **Custom AI implementation** with transformer architecture
- ⚙️ **Model management** - load and switch between different models
- 🎛️ **Customizable generation parameters** (temperature, max length, etc.)
- 📂 **File menu** for model management and settings
- 📱 **Cross-platform** compatibility (Windows, macOS, Linux)

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- CUDA-compatible GPU (recommended for training, not required for inference)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/DOAI.git
   cd DOAI
   ```

2. Create and activate a virtual environment (recommended):
   ```bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate
   
   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required packages:
   Just Run The Setup.bat File.

## Quick Start

1. **Run the application**:
 Just Run The Run.bat File Then Wait For A Few Seconds Then After A Bit the AI App Should Start.

2. **Load a pre-trained model**:
   - Go to `File > Load Model...`
   - Select a model file (`.pt`)
   - Select the corresponding tokenizer file (`.json`)

3. **Start chatting**:
   - Type your message in the input field
   - Press the send button

## Project Structure

```
DOAI/
├── data/                   # Training data and resources
│   └── train.jsonl         # Sample training data
├── models/                 # Model checkpoints and tokenizers
├── src/                    # Source code
│   ├── ai_core.py          # Core AI model implementation
│   ├── config.py           # Configuration settings
│   ├── data_loader.py      # Data loading utilities
│   ├── main.py             # Main application entry point
│   ├── tokenizer.py        # Custom tokenizer implementation
│   └── train.py            # Training script
├── requirements.txt         # Python dependencies
└── README.md               # This file
```

## Training a New Model

1. **Prepare your data**:
   - Create a JSONL file with conversation pairs in the format:
     ```json
     {"context": "User message", "response": "AI response"}
     ```
   - Or use the provided `create_dataset.py` to generate sample data

2. **Train the model**:
   ```bash
   python train.py --data_path data/train.jsonl --output_dir models/my_model
   ```
   
   Training options:
   ```
   --data_path: Path to training data file
   --output_dir: Directory to save the trained model
   --num_epochs: Number of training epochs (default: 10)
   --batch_size: Batch size for training (default: 8)
   --learning_rate: Learning rate (default: 1e-4)
   --use_cuda: Use GPU if available (default: True)
   ```

## Model Architecture

DOAI uses a transformer-based architecture with the following components:

- **Tokenizer**: Custom byte-pair encoding (BPE) tokenizer
- **Model**: Transformer encoder with multi-head self-attention
- **Training**: Teacher-forcing with cross-entropy loss
- **Inference**: Beam search or nucleus sampling


### UI Customization

The application's appearance can be customized by modifying the stylesheet in `main.py`. Look for the `setStyleSheet` method to adjust colors, fonts, and spacing.

### Model Customization

You can modify the model architecture in `ai_core.py`. The `DOAIModel` class defines the neural network architecture, and the `DOAIAssistant` class handles the high-level functionality.

## Troubleshooting

If The AI Programm Doesnt Start After A While Then Run The Run Debug.bat File To See What The Problem Is And If There Are Any Errors Or Problems Please Report Them In The Isuues Tab.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This Project Is Not Licensed But If You're Going Forking This Just Make Sure To Tag Me ;)

## Acknowledgments

- PyTorch team for the amazing deep learning framework
- Hugging Face for inspiration and reference implementations
- Apple for the design inspiration

More Updates Comming Soon. ༼ つ ◕_◕ ༽つ

## License

This project is licensed under the MIT License - see the LICENSE file for details.
