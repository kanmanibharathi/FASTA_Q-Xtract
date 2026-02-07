# FASTA-Xtract

FASTA-Xtract is a high-performance cross-platform application designed for extracting specific DNA/Protein sequences from large FASTA files using CSV-based target lists. It features a modern, fluid GUI inspired by macOS and Windows 11 aesthetics.

![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.10%2B-blue)
![Framework](https://img.shields.io/badge/framework-PyQt6-7B3F00)

## 🚀 Key Features

- **Modern UI**: Dark-mode interface with emerald highlights and glassmorphism.
- **Bulk Extraction**: Extract thousands of sequences simultaneously from multi-GB FASTA files.
- **Embedded Assets**: Fonts and icons are embedded directly into the binary for zero-dependency execution.
- **Cross-Platform**: Native standalone binaries for Windows, macOS, and Linux.

## 📥 Download (No Installation Required)

This application is available as a single, portable executable. You do not need to install Python or any dependencies.

1.  Go to the [**Releases Page**](../../releases) on GitHub.
2.  Download the file for your operating system:
        - **Windows**: `FASTA-Xtract.exe`
    - **macOS**: `FASTA-Xtract.app.zip` (Unzip and run)
    - **Linux**: `FASTA-Xtract-Linux` (Mark as executable if needed: `chmod +x FASTA-Xtract-Linux`)
    - **R app**: `FASTA-Xtract.R` (Open Using R studio)
3.  **Run**: Just double-click the downloaded file (or run from terminal) to start the application.

---

## 🛠️ Cross-Platform Build Instructions

This project is optimized for easy packaging into standalone executables. No external dependencies are required for the final user.

### 1. 🪟 Windows (Build on Windows)
Generates a `.exe` file.
- **Script**: `FASTA-Xtract.spec` (in root)
- **Commands**:
  ```powershell
  pip install pyinstaller PyQt6
  pyinstaller --clean FASTA-Xtract.spec
  ```
- **Output**: `dist/FASTA-Xtract.exe`

### 2. 🐧 Linux (Build on Linux/WSL)
Generates a standalone binary for Ubuntu/Debian/CentOS.
- **Folder**: `./linux`
- **Commands**:
  ```bash
  cd linux
  chmod +x build_linux.sh
  ./build_linux.sh
  ```
- **Output**: `linux/dist/FASTA-Xtract`

### 3. 🍎 macOS (Build on Mac)
Generates a high-resolution `.app` bundle.
- **Folder**: `./mac`
- **Commands**:
  ```bash
  cd mac
  chmod +x build_mac.sh
  ./build_mac.sh
  ```
- **Output**: `mac/dist/FASTA-Xtract.app`

---

## 🧬 Development Setup

If you want to run the code from source:

1. **Install Requirements**:
   ```bash
   pip install PyQt6
   ```
2. **Run Application**:
   ```bash
   python fasta-xtract-qt.py
   ```

## 📁 Project Structure

- `fasta-xtract-qt.py`: The master source code (Logic + UI + Embedded Assets).
- `windows/`: Windows-specific metadata and pre-built binaries.
- `linux/`: Linux build script (`build_linux.sh`) and `.desktop` shortcut integration.
- `mac/`: macOS build configuration (`FASTA-Xtract-Mac.spec`) and app icons.
- `Rapp/`: Legacy R-based core for research reference.

## ⚖️ License
This project is proprietary for One Research Hub. All rights reserved.
