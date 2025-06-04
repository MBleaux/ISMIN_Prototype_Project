# ISMIN Prototype Project – Air Guitar 🎸

This project is a prototype of an **Air Guitar**, developed as part of the *Prototyping Project* in the **Microelectronics and Computer Science** program at the **École des Mines de Saint-Étienne – ISMIN**.

## 🛠️ Overview

The system uses an **STM32F301K8T6** microcontroller to simulate a guitar. It captures the frequency of a conditioning circuit connected to a metal plate and outputs a **PWM signal** corresponding to a musical note, depending on which buttons are pressed — effectively mimicking the action of "strumming" and "fretting" a guitar string.

### 🧩 Main Components:
- **Timers 1 and 2**: used for frequency capture and PWM generation
- **UART**: for serial communication (e.g., debugging, monitoring)
- **GPIOs**: for reading input from buttons and controlling outputs

## ⚙️ Functional Description

The embedded code implements the following main features:

- `HAL_TIM_IC_CaptureCallback`:  
  Callback function used to **capture the input frequency** from the metal plate via the conditioning circuit.

- `Check_Frequency`:  
  Determines whether the captured frequency is **below 42kHz**, indicating the **presence of a hand or body** near the metal plate.

- `Check_Pin`:  
  Reads the **state of input buttons**, simulating different frets or chords on a guitar neck.

- `Config_PWM`:  
  Configures and generates a **PWM output signal** with a frequency corresponding to the selected musical note.

## 📁 Project Structure

- **`PP`**: Prototyping Project codes
- **`Rapport-ProjetPrototypage.pdf`**: documentation of the project