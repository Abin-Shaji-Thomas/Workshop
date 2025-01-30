# SAM 2 Workshop Setup Guide for Windows and Ubuntu Users

## Prerequisites
- Python 3.10 or higher
- Git
- pip
- Virtual environment support

---

## **Windows Installation Steps**

### **1. Prepare Windows Environment**
```powershell
# Open PowerShell as Administrator
mkdir sam2_workshop
cd sam2_workshop
```

### **2. Install Python**
- Download Python 3.10+ from the [official Python website](https://www.python.org/).
- Ensure **"Add Python to PATH"** is checked during installation.

### **3. Clone SAM 2 Repository**
```powershell
git clone https://github.com/facebookresearch/sam2.git
cd sam2
```

### **4. Create Virtual Environment**
```powershell
python -m venv sam2_env
sam2_env\Scripts\activate
```

### **5. Install Dependencies**
```powershell
pip install torch torchvision
pip install -e ".[notebooks]"
pip install jupyter
pip install ipykernel
python -m ipykernel install --user --name=sam2_env 
```

### **6. Download Checkpoints**
```powershell
cd checkpoints
./download_ckpts.sh
cd ..
```
If you face permission issues, try:
```powershell
Set-ExecutionPolicy Unrestricted -Scope Process
./download_ckpts.sh
```

### **7. Launch Jupyter Notebook**
```powershell
jupyter notebook
```

---

## **Ubuntu Installation Steps**

### **1. Update System**
```bash
sudo apt update
sudo apt install python3-pip python3-venv git
```

### **2. Create Workshop Directory**
```bash
mkdir sam2_workshop
cd sam2_workshop
```

### **3. Clone SAM 2 Repository**
```bash
git clone https://github.com/facebookresearch/sam2.git
cd sam2
```

### **4. Install Python 3.12**
```bash
sudo apt install python3.12-venv
```

### **5. Create Virtual Environment**
```bash
python3 -m venv sam2_env
source sam2_env/bin/activate
```

### **6. Install Dependencies**
```bash
pip install torch torchvision
pip install -e ".[notebooks]"
pip install jupyter
pip install ipykernel
python -m ipykernel install --user --name=sam2_env 
```

### **7. Download Checkpoints**
```bash
cd checkpoints
chmod +x download_ckpts.sh
./download_ckpts.sh
cd ..
```
If you face permission issues, try:
```bash
sudo chmod +x download_ckpts.sh
sudo ./download_ckpts.sh
```

### **8. Launch Jupyter Notebook**
```bash
jupyter notebook
```

---

## **Important Notes**
- Always **activate the virtual environment** before working.
- For Windows, consider using **Windows Subsystem for Linux (WSL)** for better compatibility.
- Verify Python version:
  ```powershell
  python --version
  ```

## **Troubleshooting**
- **Upgrade pip:**
  ```bash
  python -m pip install --upgrade pip
  ```
- **For GPU support, ensure compatible CUDA and PyTorch versions.**
- **Check CUDA availability:**
  ```bash
  python -c "import torch; print(torch.cuda.is_available())"
  ```

## **GPU Recommendations**
- **Recommended GPU:** NVIDIA with CUDA support
- **Suggested CUDA version:** 12.1
- **Verify GPU compatibility before installation**

⚠ **Warning:** Installation steps may vary slightly based on system configurations.

