
# ESP32-CAM-Video-Stream-External-WiFi

## Overview
This project enables users to access the camera feed via the HTTP protocol at a local IP address within the same network by configuring the board to connect to an external Wi-Fi network. Users can connect a device to the board's Wi-Fi, input the target Wi-Fi credentials, and subsequently establish a connection to the specified network.

## Features
- **Wi-Fi Configuration**: Connect  ESP32's to external Wi-Fi credentials Using a web page.
- **Video Streaming**: Stream video from the ESP32-CAM at local IP.


## Requirements

To get started, you'll need the following components:

- **One ESP32-CAM (Ai Thinker)**
- **One USB to TTL Converter or FTDI Module**
- **Female-to-female jumper wires**

## Wiring Configuration

To connect your `ESP32-CAM` to the `USB to TTL` converter or `FTDI` module, follow the wiring configuration below:

| ESP32-CAM       | USB to TTL or FTDI Programmer |
|------------------|------------------------------|
| GND              | GND                          |
| 3.3V             | VCC                          |
| U0R              | TX                           |
| U0T              | RX                           |


### Important Notes

- **GPIO 0** must be connected to **GND** in `ESP32-CAM` to upload a sketch.
- After connecting **GPIO 0 to GND**, press the ESP32-CAM on-board **RESET** button to put your board in flashing mode.



## Getting Started

1. **Clone this repository:**

   ```bash
   git clone https://github.com/pezhvak98/ESP32-CAM-Video-Stream-External-WiFi.git
After cloning, you can use the code as you like.



2.  **Install the required libraries:**
    
    Make sure you have the necessary libraries installed in your Arduino IDE. 
    Add this URL in ‍`File > Preference > Additional Board Manager` :
    ```bash
    https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json   
    ```
    
3.  **Upload the sketch:**
    
    Open the provided Arduino sketch in the Arduino IDE, select the appropriate board and port, and upload it.
    
4.  **Connect to the ESP32-CAM Wi-Fi:**
    
    Once the upload is complete, disconnect `GPIO 0` from `GND `and `reset` the **ESP32-CAM**. It will start broadcasting a Wi-Fi signal. Connect to it using your smartphone or computer using `192.168.4.1`.

5.  **Enter the external Wi-Fi name and password**
    Enter the Wi-Fi **SSID** and  **password** correctly and submit the form. Remember, **immediately** after submitting the form, your connection with the board's internal Wi-Fi will be disconnected. Because the board is out of access point mode and is connected to another Wi-Fi.
    
6.  **Access the video stream :**
    
    Open a web browser and enter the IP address provided in the serial monitor to view the video stream.
     you can see the local IP in **Serial Monitor**.
     ```python
     #Default Local IP Address
     192.168.1.106/stream    
     ```

## Note on Pending Features

This project requires further refinement. While the core functionality is operational, some enhancements and fixes have not yet been implemented. We appreciate your understanding.

> You can refer to a [ESP32-CAM-Video-Stream-Internal-WiFi ](https://github.com/pezhvak98/ESP32-CAM-Video-Stream-Internal-WiFi) where the video is shared using internal Wi-Fi instead.
---
```vbnet
	**	Feel free to modify any sections to better fit your project specifics! **
```
