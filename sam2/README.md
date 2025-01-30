## SAM 2 Workshop Setup Guide for Windows and Ubuntu Users

### Prerequisites
- Python 3.10 or higher
- Git
- pip
- Virtual environment support

### Windows Installation Steps

1. **Prepare Windows Environment**
```powershell
# Open PowerShell as Administrator
mkdir sam2_workshop
cd sam2_workshop
```

2. **Install Python**
- Download Python 3.10+ from official Python website
- Ensure "Add Python to PATH" is checked during installation

3. **Clone SAM 2 Repository**
```powershell
git clone https://github.com/facebookresearch/sam2.git
cd sam2
```

4. **Download Python 3.12**
```bash
sudo apt install python3.12-venv
```

5. **Create Virtual Environment**
```powershell
python -m venv sam2_env
sam2_env\Scripts\activate
```

6. **Install Dependencies**
```powershell
pip install torch torchvision
pip install -e ".[notebooks]"
pip install jupyter
pip install ipykernel
python -m ipykernel install --user --name=sam2_env --display-name "Python (sam2_env)"
```

### Launch Jupyter Notebook
```bash
# For both Windows and Ubuntu
jupyter notebook
```

### Ubuntu Installation Steps

1. **Update System**
```bash
sudo apt update
sudo apt install python3-pip python3-venv git
```

2. **Create Workshop Directory**
```bash
mkdir sam2_workshop
cd sam2_workshop
```

3. **Clone SAM 2 Repository**
```bash
git clone https://github.com/facebookresearch/sam2.git
cd sam2
```

4. **Download Python 3.12**
```bash
sudo apt install python3.12-venv
```

5. **Create Virtual Environment**
```bash
python3 -m venv sam2_env
source sam2_env/bin/activate
```

6. **Install Dependencies**
```bash
pip install torch torchvision
pip install -e ".[notebooks]"
pip install jupyter
pip install ipykernel
python -m ipykernel install --user --name=sam2_env --display-name "Python (sam2_env)"
```

### Launch Jupyter Notebook
```bash
# For both Windows and Ubuntu
jupyter notebook
```

### Important Notes
- Always activate virtual environment before working
- For Windows, consider using Windows Subsystem for Linux (WSL) for better compatibility
- Verify Python version: `python --version`

### Troubleshooting
- Upgrade pip: `python -m pip install --upgrade pip`
- For GPU support, ensure compatible CUDA and PyTorch versions
- Check CUDA availability: 
```python
python -c "import torch; print(torch.cuda.is_available())"
```

### GPU Recommendations
- Recommended GPU: NVIDIA with CUDA support
- Suggested CUDA version: 12.1
- Verify GPU compatibility before installation

**Warning**: Installation may vary slightly based on specific system configurations.

