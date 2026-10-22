# ✈️ Realtime Airfoil CFD (Computational Fluid Dynamics)

Welcome back! Let's explore how air flows over airplane wings in real-time! 🚀

## 🏎️ ELI5: What is this? (Explain Like I'm 5)

Imagine you are in a moving car and stick your hand out the window 🚗💨:

* If you hold your hand **flat**, the air glides over it smoothly.

* If you **tilt** your hand up, the air pushes your hand upward! 🖐️⬆️

* If you tilt it **too much**, your hand gets slapped backward! 💥

This project uses a computer brain 🧠 (AI) to show you **how the air moves around a wing instantly**, without waiting hours for heavy science calculations! ⚡

## 🛠️ Project Repository & Quick Setup

### 📂 Directory Structure

```text
realtime-airfoil-cfd/
├── .gitignore
├── README.md
├── requirements.txt
├── config/
│   └── config.yaml
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── 01_exploratory_analysis.ipynb
├── models/
│   ├── saved/
│   └── checkpoints/
├── src/
│   ├── __init__.py
│   ├── data_processing.py
│   ├── cfd_solver.py
│   ├── model.py
│   └── visualization.py
├── app/
│   ├── app.py
│   └── templates/
└── tests/
    └── test_cfd.py
```

---

### 💻 Setup Files

#### `.gitignore`
```text
# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class

# C extensions
*.so

# Distribution / packaging
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
*.egg-info/
.installed.cfg
*.egg

# Virtual environments
venv/
env/
ENV/
env.bak/
venv.bak/

# Data & Large Files
data/raw/*
data/processed/*
!data/raw/.gitkeep
!data/processed/.gitkeep

# Saved Models & Weights
models/saved/*
models/checkpoints/*
!models/saved/.gitkeep
!models/checkpoints/.gitkeep

# Jupyter Notebook Checkpoints
.ipynb_checkpoints

# Environment variables
.env
.env.local

# IDEs & Editors
.vscode/
.idea/
*.swp
*.swo

# OS files
.DS_Store
Thumbs.db
```

#### `requirements.txt`
```text
# Core Scientific & Data Processing
numpy>=1.24.0
scipy>=1.10.0
pandas>=2.0.0

# Deep Learning & ML
torch>=2.0.0
torchaudio
torchvision

# CFD & Mesh Generation (Optional/Helper libraries)
meshio>=5.3.0
pyvista>=0.38.0

# Visualization & Interactive App
matplotlib>=3.7.0
plotly>=5.14.0
streamlit>=1.22.0

# Utilities
pyyaml>=6.0
tqdm>=4.65.0

# Testing & Code Quality
pytest>=7.3.0
black>=23.3.0
```

---

### ⚡ PowerShell Quick Setup Script

Run this in your PowerShell terminal to generate the folders and baseline files automatically:

```powershell
# Create root directory and navigate inside
New-Item -ItemType Directory -Name "realtime-airfoil-cfd" -Force
Set-Location "realtime-airfoil-cfd"

# Create folder structure
$folders = @(
    "config",
    "data/raw",
    "data/processed",
    "notebooks",
    "models/saved",
    "models/checkpoints",
    "src",
    "app/templates",
    "tests"
)

foreach ($folder in $folders) {
    New-Item -ItemType Directory -Path $folder -Force
}

# Create starter files
$files = @(
    ".gitignore",
    "README.md",
    "requirements.txt",
    "config/config.yaml",
    "notebooks/01_exploratory_analysis.ipynb",
    "src/__init__.py",
    "src/data_processing.py",
    "src/cfd_solver.py",
    "src/model.py",
    "src/visualization.py",
    "app/app.py",
    "tests/test_cfd.py"
)

foreach ($file in $files) {
    New-Item -ItemType File -Path $file -Force
}

Write-Host "Realtime Airfoil CFD project directory set up successfully!" -ForegroundColor Green
```

---

## 🎮 Interactive Experiments: Try It Yourself!

| 🎛️ Control | 🧪 What to Change | 📊 What Happens? | 
| ----- | ----- | ----- | 
| **Angle of Attack (Tilt)** | Increase to $15^\circ$ | Watch lift go UP 📈 until it suddenly stalls 📉! | 
| **Wind Speed** | Boost velocity $v$ | Colors turn red 🔥 (high speed / low pressure)! | 
| **Wing Shape** | Pick a curved airfoil | Notice how top air moves faster than bottom air 🌬️! | 

## ❓ Mini Quick Quiz!

> **Why does an airplane lift up into the sky?**
>
> * **A)** The air under the wing pushes harder than the fast air on top! 🎈
> * **B)** Magic Invisible Strings ✨
> * **C)** The engines push directly down 🛞
>
> *(Hint: It's **A**! Bernoulli's principle at work! Bernoulli says: Fast air = lower pressure!)*
