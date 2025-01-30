# YOLO Setup Guide for Beginners on Ubuntu

Welcome to the YOLO (You Only Look Once) setup guide! This document will help you install and set up the YOLO environment on Ubuntu, making it easy for complete beginners to get started with object detection and image segmentation using YOLO models.

## Prerequisites

Before you begin, ensure that you have the following installed on your system:
- Python 3.8 or higher
- Git
- pip
- Virtual environment support

## Step-by-Step Installation

For GPU support, confirm that compatible CUDA and PyTorch versions are installed.

---

### For Windows

#### 1. Install Python and Git

Download and install Python from [python.org](https://www.python.org/downloads/) (ensure to check "Add Python to PATH"). Also, download and install Git from [git-scm.com](https://git-scm.com/download/win).

#### 2. Open Command Prompt

Open Command Prompt (cmd) or PowerShell.

#### 3. Create a Project Directory

Create a directory for your YOLO project:

```
mkdir yolo_project
cd yolo_project
```

#### 4. Clone the YOLO Repository

Clone the Ultralytics YOLO repository from GitHub:

```
git clone https://github.com/ultralytics/ultralytics.git
cd ultralytics
```

#### 5. Create a Virtual Environment

Create a virtual environment to manage dependencies:

```
python -m venv yolo_env
.\yolo_env\Scripts\activate # Activate the environment
```

#### 6. Install Dependencies

With your virtual environment activated, install the required packages:

```
pip install -r requirements.txt
```

### 7. Launch Jupyter Notebook (Optional)

If you want to use Jupyter Notebook for running YOLO examples, install Jupyter:

```
pip install jupyter
jupyter notebook # This will open the Jupyter interface in your web browser.
```

## Important Notes for Windows Users

- Ensure you're inside the activated virtual environment before running commands.
- The `jupyter notebook` command will open a web browser interface with available notebooks.

## Troubleshooting for Windows Users

If facing installation issues, verify Python and pip versions.

Ensure you have the latest pip version:

```
python -m pip install --upgrade pip
```


## For Ubuntu

### 1. Update Your System

Open a terminal and run the following commands to update your package list:

```bash
sudo apt update
sudo apt upgrade
```

### 2. Install Required Dependencies

Install Python and other necessary packages:
```
sudo apt install python3 python3-venv python3-pip git

```
### 3. Create a Project Directory

Create a directory for your YOLO project:
```
mkdir yolo_project 

cd yolo_project
```
### 4. Clone the YOLO Repository

Clone the Ultralytics YOLO repository from GitHub:
```
git clone https://github.com/ultralytics/ultralytics.git

cd ultralytics
```

### 5. Create a Virtual Environment

Create a virtual environment to manage dependencies:
```
python3 -m venv yolo_env

source yolo_env/bin/activate # Activate the environment
```

### 6. Install Dependencies

With your virtual environment activated, install the required packages:
```
pip install -r requirements.txt 
```
### 7. Launch Jupyter Notebook (Optional)

If you want to use Jupyter Notebook for running YOLO examples, install Jupyter:
```
pip install jupyter
jupyter notebook # This will open the Jupyter interface in your web browser.
```

## Important Notes

- Ensure you're inside the activated virtual environment before running commands.
- The `jupyter notebook` command will open a web browser interface with available notebooks.
- Recommended to use Windows Subsystem for Linux (WSL) if on Windows for best compatibility.

## Troubleshooting

If facing installation issues, verify Python and pip versions.

Ensure you have the latest pip version:

```
python -m pip install --upgrade pip
```

For GPU support, confirm that compatible CUDA and PyTorch versions are installed.

## Conclusion

You are now set up to start using YOLO for object detection tasks! Explore the various tutorials and examples provided in the repository to get familiar with its capabilities.








