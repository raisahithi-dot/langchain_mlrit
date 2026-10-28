# 8086 Stepper Motor Virtual Lab

A software-only educational project that helps students understand an 8086 stepper-motor practical.

## Features

- Step-by-step 8086 trainer procedure reference
- Virtual connection checklist
- 8255 PPI Control Word Register (CWR) bit decoder
- Explanations of assembly instructions and reference opcodes
- Mnemonic-entry practice
- Illustrative clockwise and anticlockwise motor pointer animation
- Viva questions and practical-record summary

## Run in Google Colab

1. Upload `8086_Stepper_Motor_Virtual_Lab.ipynb` to Google Drive, or open it from GitHub in Google Colab.
2. Open the notebook.
3. Choose **Runtime → Run all**.
4. Follow the sections from top to bottom.

The notebook uses Python and `ipywidgets`. Colab generally supports widgets in notebook output. If widgets do not display, refresh the page and reconnect the runtime.

## Files

- `8086_Stepper_Motor_Virtual_Lab.ipynb` — complete runnable notebook
- `requirements.txt` — Python package dependencies
- `.gitignore` — common files to exclude from Git

## Important technical note

This is a teaching simulation only. It does not connect to or control physical hardware, and it is not a cycle-accurate 8086 emulator. The assembly listing and I/O addresses are based on the student-provided practical text and must be checked against the actual trainer manual.

In particular, `MOV AL,80H` and `MOV AL,88H` load bytes into AL; they are not automatically 8255 CWR writes. The destination port address in `OUT DX,AL` determines where the byte is sent. The CWR decoder explains standard 8255 formats when the byte is actually written to the 8255 control-register address.

## Suggested GitHub repository description

**Software-only 8086 stepper motor virtual lab with 8255 CWR bit decoder, assembly instruction tutor, trainer procedure guide, and motor animation.**
