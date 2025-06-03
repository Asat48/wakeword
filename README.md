# Wake Word Detection on Arduino using Edge Impulse

This project implements a wake word detection system on an Arduino board using Edge Impulse's inferencing engine and a PDM microphone. The system continuously listens for a specific wake word and toggles an LED indicator when the wake word is detected with high confidence.

---

## Video Reference

This implementation is based entirely on the video by DigiKey:
**[How to Do Speech Recognition with Arduino | Digi-Key Electronics](https://www.youtube.com/watch?v=fRSVQ4Fkwjc&t=1s)**

---

## Features

Real-time audio inferencing
Edge Impulse SDK integration
Wake word detection with confidence threshold
LED indicator on wake word detection
Double-buffering to ensure smooth audio capture

---

## Hardware Requirements

* Arduino board (e.g., Arduino Nano 33 BLE Sense or similar with PDM microphone support)
* LED (or use the built-in LED pin)

---

## How It Works

1. **Audio Capture:**

   * Uses the built-in PDM microphone to continuously record audio.

2. **Edge Impulse Classifier:**

   * Uses the pre-trained model generated in Edge Impulse Studio.
   * Classifier continuously analyzes short audio slices.

3. **Wake Word Detection:**

   * If the classifier detects the wake word with a confidence above **0.7**, it turns on the LED.
   * Otherwise, the LED stays off.

4. **Output:**

   * Classification results and timing stats are printed to the serial monitor.

---

## Setup & Installation

1. **Clone the Repository:**

```bash
git clone https://github.com/Asat48/wakeword.git
```

2. **Open in Arduino IDE:**

   * Open `wakeword_detection.ino` in the Arduino IDE.
   * Make sure your board is selected in the **Tools > Board** menu.

3. **Install Required Libraries:**

   * Install the **PDM** library via the Library Manager.

4. **Upload the Code:**

   * Connect your Arduino board via USB.
   * Click the **Upload** button in the Arduino IDE.

5. **Open Serial Monitor:**

   * Set the baud rate to **115200** 

---

## Model & Edge Impulse Project

This project assumes that you have already created and trained your wake word detection model in Edge Impulse Studio. Make sure to:

**Train your model** on your chosen wake word data.
**Deploy** the model as an Arduino library.
**Include** the model files in this project (e.g., `model_metadata.h` and accompanying `.cpp`/`.h` files).

---

## Resources

* [Edge Impulse](https://www.edgeimpulse.com/)
* [Arduino PDM Library](https://www.arduino.cc/en/Reference/PDM)

---

## License

This project is for **educational purposes** and follows the original licensing terms of the referenced video and the Edge Impulse examples.

---
