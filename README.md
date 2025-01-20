
# Ondroid Robotics Developer Test Assignment

This repository contains the solutions for the Ondroid Robotics Developer Test Assignment. 
The task involves programming an ESP32 microcontroller connected to a 10-segment LED digital strip 
and using Python with OpenCV for computer vision analysis.

---

## Assignment Overview

The goal is to:
1. **ESP32 Code (C++)**: Control the 10-segment LED strip to randomly turn segments on or off.
2. **Python Code**: Analyze an image of the LED strip using OpenCV to count how many segments are lit.

The assignment verifies both hardware control and software-based analysis capabilities.

---

## Folder Structure

```
/
|-- esp32_code/          # Contains the C++ code for controlling the LED strip
|-- python_code/         # Contains the Python script for LED counting
|-- assignment_output/   # Video showing the output of given code by robot
|-- README.md            # This file
```

---

## Instructions

### 1. C++ Code (ESP32)

- The C++ code is located in the `esp32_code/` folder.
- It configures 10 GPIO pins on the ESP32 for controlling each LED segment.
- The `setup()` function initializes the pins as output.
- The `loop()` function randomly turns LED segments on or off at 1-second intervals.

### 2. Python Code (OpenCV)

- The Python script is located in the `python_code/` folder.
- It uses OpenCV to process an input image of the LED strip and count the number of lit segments.
- Steps in the script:
  1. Convert the image to grayscale.
  2. Apply a binary threshold to isolate bright areas (lit LEDs).
  3. Use contour detection to identify and count lit segments based on size filtering.

---

## Usage

### Setting Up the ESP32
1. Open the Arduino IDE and upload the `esp32_code.ino` file to your ESP32.
2. Connect the LED strip to the ESP32 using the following pin mapping:
   - GPIO 27: Segment 1
   - GPIO 25: Segment 2
   - GPIO 33: Segment 3
   - GPIO 21: Segment 4
   - GPIO 26: Segment 5
   - GPIO 23: Segment 6
   - GPIO 22: Segment 7
   - GPIO 12: Segment 8
   - GPIO 19: Segment 9
   - GPIO 13: Segment 10
3. Observe the LED strip as segments light up randomly.

### Running the Python Script
1. Capture an image of the LED strip after running the ESP32 code.
2. Save the image as `led_matrix.jpg` (or update the path in the script).
3. Run the Python script:
   ```bash
   python count_leds.py
   ```
4. The script will output the number of lit LEDs in the console.

---

## Example Output

- **C++ Code Output**: LED segments randomly turning on and off.
- **Python Script Output**: A message like `Number of LEDs turned on: 6`.

---

## Notes

- The Python script uses contour area filtering to avoid noise. Adjust the size range in the code if needed for your setup.
- Ensure proper lighting conditions when capturing the image for accurate results.

---

## Submission

- Submit this repository as a public GitHub link.
- Include the following:
  1. ESP32 C++ code
  2. Python script
  3. Assignment_output

---

## Disclaimer

This code is created specifically for the Ondroid Robotics Developer Test Assignment. Use the repository as-is to replicate the results.
