# Cipher Encoding System (Substitution + Polybius)

This repository provides a Python-based implementation of a classical cryptography simulation system. It demonstrates how traditional encryption techniques such as a substitution cipher and a Polybius cipher can be combined into a structured, ordered encryption pipeline with a graphical user interface.

The project is designed for educational purposes, focusing on modular programming, algorithm design, and basic cryptographic principles.

---

# System Overview

This cipher system simulates classical encryption using:

- A **Substitution Cipher** based on a user-defined keyword
- A **Polybius Cipher (5×5 grid system)**
- A **Cipher Engine** for ordered execution of encryption steps
- A **Tkinter GUI** for file-based interaction

All components are designed to work together in a reversible encryption pipeline.

---

# Cipher Architecture

## 1. File Handling Module
- Reads `.txt` files from disk
- Writes encoded or decoded output files
- Acts as the bridge between user input and cipher system

## 2. Substitution Cipher
- Uses a keyword-based shuffled alphabet
- Replaces each letter with a mapped equivalent
- Acts as the first encryption layer

## 3. Polybius Cipher (5×5 Grid)
- Converts letters into coordinate pairs (row, column)
- Uses a fixed 5×5 grid (25 characters)
- Merges **J → I** to maintain grid compatibility
- Produces numeric encoded output

## 4. Cipher Engine
- Controls encryption order
- Supports chained execution:
  - Substitution → Polybius
- Ensures reverse execution for decoding

## 5. Tkinter GUI
- File selection system
- Codeword input field
- Encode / Decode buttons
- Output display window

---

# Design Principles

This project follows key software design principles:

- **Modularity**: Each cipher is implemented as a separate class
- **Reversibility**: Every encryption step supports decoding
- **Consistency**: Shared alphabet system (A–Z with J merged into I)
- **Extensibility**: New cipher methods can be added easily
- **Usability**: GUI interface replaces command-line interaction

---

# Installation Requirements

- Python 3.x
- No external libraries required

Built-in modules used:
- `tkinter`
- `sys`

---

# Usage

## 1. Run the program
```bash
python main.py
