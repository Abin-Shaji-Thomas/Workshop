## SAM 2 Workshop Setup Guide for Windows and Linux Users

### Prerequisites
- Python 3.10 or higher
- Git
- pip
- Virtual environment support

### Step-by-Step Installation

1. **Create Workshop Directory**
```bash
mkdir sam2_workshop
cd sam2_workshop
```

2. **Clone the Repository**
```bash
git clone https://github.com/facebookresearch/sam2.git
cd sam2
```

3.**Update your system**
```bash
sudo apt update
```

4. **Download Python 3.12**
```bash
sudo apt install python3.12-venv
```

5. **Create Virtual Environment**

   **For Linux/macOS**
```bash
python3 -m venv sam2_env
source sam2_env/bin/activate
```
  **For Windows**
  
```bash
python -m venv sam2_env
sam2_env\Scripts\activate
```

6. **Install Dependencies**
```bash
pip install -e .
pip install -e ".[notebooks]"
```

7. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

### Important Notes
- Ensure you're inside the activated virtual environment before running commands
- The `jupyter notebook` command will open a web browser interface with available notebooks
- Recommended to use Windows Subsystem for Linux (WSL) if on Windows for best compatibility

### Troubleshooting
- If facing installation issues, verify Python and pip versions
- Ensure you have the latest pip: `python -m pip install --upgrade pip`
- For GPU support, confirm compatible CUDA and PyTorch versions are installed

