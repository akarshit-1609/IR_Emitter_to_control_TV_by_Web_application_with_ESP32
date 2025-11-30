# IR TV Remote Control for DD Free Dish Set-top box with ESP32 (PlatformIO)

This project for send IR signals to the set-top box by acting as an IR remote with Web interface.

---

## Features

- Use smartphone as an IR Remote with connected to ESP32 web server.
- Send IR commands to control TV power, volume, channel, etc.

---

## Hardware Required

- ESP32 development board
- IR Emitter LED
- DD Free Dish set-top box running on TV
- Jumper wires
- Breadboard (optional)

---


## Getting Started

1.  **Clone the repository:**

    Open your terminal or command prompt and use the following command to clone the project:

    ```bash
    git clone https://github.com/akarshit-1609/IR_Emitter_to_control_TV_by_Web_application_with_ESP32.git
    ```

2.  **Open in PlatformIO:**

    Open the cloned project in your preferred IDE with the PlatformIO extension installed (e.g., VS Code).

3.  **Configure Variables:**

    Before uploading the code to your ESP32, you need to configure some variables, particularly the GPIO pin connected to your ir emitter led.

    *   **Locate the configuration:** Open the `src/main.cpp` file.
    *   **Find the variable:** Look for a line similar to this:

        ```c++
        const char* ssid = "Your_ssid";// Replace with your custom ssid
        const char* password = "your_password"; // Replace with your password

        const int ir = 21; // Replace with your sensor GPIO pin
        ```

    *   **Replace the value:** Change the `21` to the actual GPIO pin number where your signal pin is connected on your ESP32 board. Refer to your ESP32 board's pinout diagram if you are unsure.

4.  **Build and Upload:**

    *   Connect your ESP32 board to your computer via USB.
    *   In PlatformIO, click the "Build" button to compile the project.
    *   Click the "Upload" button to upload the compiled code to your ESP32.

---

## Project Structure

*   `platformio.ini`: PlatformIO configuration file.
*   `src/main.cpp`: The main source code file.
*   `lib/`: (Optional) Directory for external libraries.

---


## Usage

Once the code is uploaded, connect any device with esp32 wifi by ssid and password given in the code after open the browser and Go to url http://192.168.0.1 and click button for control TV. Remember IR Emitter LED pointed to the dd free dish set-top box for send ir signal.

---

## Demo

https://github.com/user-attachments/assets/c2908d39-07e9-48ba-b319-555be1b3d2b5

[![Watch on YouTube](https://img.shields.io/badge/-Watch%20on%20YouTube-red?style=flat&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=hIusNPH1iok?si=2qCWpLeTFquyrPPU)

---

## Troubleshooting

- Make sure the IR Emitter LED is properly connected.
- Ensure the correct GPIO pin is used and configured as output.
- Ensure the IR LED is aligned properly towards the dd free dish set-top box.

---

## References

- [IRremoteESP8266 Library](https://github.com/crankyoldgit/IRremoteESP8266)
- [ESPAsyncWebServer Library](https://github.com/esphome/ESPAsyncWebServer)
- [ESP32 Documentation](https://docs.espressif.com/projects/esp-idf/en/latest/)
