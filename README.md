# Arduino-HomeKit-ESP32
**[Deprecated]** Native Apple HomeKit accessory implementation for the ESP32 Arduino core.

This Arduino library is a native Apple HomeKit accessory implementation for the [ESP32 Arduino core](https://github.com/espressif/arduino-esp32), and works without any additional bridges.

This library is the ESP32 version of [Arduino-HomeKit-ESP8266](https://github.com/Mixiaoxiao/Arduino-HomeKit-ESP8266), and **will no longer be maintained**, since Espressif has published the official HomeKit library for ESP32, available on Espressif's GitHub repository [esp-apple-homekit-adk](https://github.com/espressif/esp-apple-homekit-adk).

## Notes

* This is a "only-can-work" version for ESP32, remains something to be optimized.

* The `WolfSSL` used for ESP32 is based on `4.3.0-stable` version with **Hardware Acceleration Support** (enabled by default).

* The HomeKit running on ESP32 has a **GREAT PERFORMANCE** which Pair-Setup can be done in ~1.2s and Pair-Verify in < 0.1s (10x faster than ESP8266).

* The HomeKit storage on ESP32 is based on `nvs`.

## Performance WITH Hardware Acceleration on ESP32

* Preinit: ~0.53s
* Pair Setup Step 1/3: ~0s (The heavy crypto computation is done in Preinit)
* Pair Setup Step 2/3: ~0.53s 
* Pair Setup Step 3/3: ~0.20s 
* Pair Verify Step 1/2: ~0.05s
* Pair Verify Step 2/2: ~0.02s

## Performance WITHOUT Hardware Acceleration on ESP32

* Preinit: ~2.2s
* Pair Setup Step 1/3: ~0s (The heavy crypto computation is done in Preinit)
* Pair Setup Step 2/3: ~2.5s 
* Pair Setup Step 3/3: ~0.1s 
* Pair Verify Step 1/2: ~0.06s
* Pair Verify Step 2/2: ~0.03s

## Setup code of the example sketch

``111-11-111``

## Manual Installation 

Refer to the official guide: [Manual installation](https://www.arduino.cc/en/guide/libraries#toc5)
Note: this library will not publish the release version for Arduino IDE. 


#### Manual Installation for Windows

1. Click on _"Clone or Download"_ button, then click _"[Download ZIP](https://github.com/Mixiaoxiao/Arduino-HomeKit-ESP32/archive/master.zip)"_ on the page.
1. Extract the contents of the downloaded zip file.
1. Rename the extracted folder to _"Arduino-HomeKit-ESP32"_.
1. Move this folder to your libraries directory. (under windows: `C:\Users\<USERNAME>\Documents\Arduino\libraries\`)
1. Restart your Arduino IDE.
1. Check out the examples.


