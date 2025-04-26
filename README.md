# Voice Wake Word Detection on STM32

Real-time embedded AI project that detects voice keywords on STM32 microcontrollers using lightweight neural networks.  
This project captures audio from an I2S microphone, extracts MFCC features, and classifies wake words using a TinyML model.

## ✨ Features

- Real-time audio capture using I2S interface.
- MFCC (Mel Frequency Cepstral Coefficient) feature extraction.
- TinyML-based wake word detection with TensorFlow Lite Micro.
- Low-latency and low-memory footprint, suitable for STM32 MCUs.
- Wake-up actions: toggle LEDs or send UART messages upon keyword detection.

## 📷 Demo

*(Coming soon)*  
*(Add GIF or video when available.)*

## 🛠 Hardware Requirements

- STM32 Development Board (e.g., STM32F401RE Nucleo, STM32F746G-DISCO)
- I2S Microphone Module (e.g., INMP441, SPH0645LM4H)
- USB-UART Module (optional, for debug output)
- LEDs / Buttons (optional for action trigger)

## ⚙️ Software Requirements

- STM32CubeIDE or STM32CubeMX
- arm-none-eabi-gcc toolchain
- Python 3.x (for model training and conversion)
- TensorFlow and TensorFlow Lite libraries

## 🚀 Getting Started

### 1. Hardware Setup
- Connect the I2S microphone to the STM32 development board according to the I2S pinout.
- (Optional) Connect UART pins to PC for debug messages.

### 2. Firmware Build
- Clone this repository:
  ```bash
  git clone https://github.com/your_username/VoiceWakeWordDetection.git
  Open project with STM32CubeIDE or build using Makefile
  Flash the compiled firmware to your STM32 board.
  ```
  
### 3. Train a Custom Model (Optional)

Use the provided train_model.ipynb notebook to train a keyword spotting model.
Export the model to TensorFlow Lite format (.tflite) and place it under the Model/ directory.

### 4. Run and Test

Power up the board.
Speak predefined keywords near the microphone.
Observe the actions triggered (e.g., LED toggling, UART message).

## 🧠 Model Details

Input: MFCC feature vectors extracted from audio frames.
Model Type: Small CNN (Convolutional Neural Network).
Output: Softmax probability distribution over predefined keywords.

## 📚 References

[TensorFlow Lite for Microcontrollers](https://www.tensorflow.org/lite/microcontrollers)

[TinyML: Machine Learning with TensorFlow Lite on Arduino and Ultra-Low-Power Microcontrollers](https://www.oreilly.com/library/view/tinyml/9781492052043/)

## 📈 Future Work

Add multi-keyword detection.
Implement noise-robust feature extraction.
Optimize model size and inference speed.
Add support for low-power sleep/wake cycles.

## 📜 License

This project is licensed under the MIT License.
See the LICENSE file for details.

## ✍️ Author
 
[PhamNgocTrieu](https://github.com/nt-mil)
