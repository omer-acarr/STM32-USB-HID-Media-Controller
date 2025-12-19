# STM32 USB HID Media Controller (Volume/Mute)

This project is a driverless USB HID application developed for STM32 microcontrollers that allows you to control your computer's volume (Volume Up/Down/Mute).

Based on the “Consumer Control” structure in the open-source `diabolo38/HidKbd` project, it is an embedded software solution optimized solely for multimedia control, stripped of unnecessary keyboard functions.

## 🎯 Technical Purpose of the Project
It was developed to analyze the complex structure of the USB protocol and the **Device Class Definition for HID** standard. It focuses particularly on the following topics:

* **USB Report Descriptors:** Analysis of the differences in descriptors between a standard keyboard and a Media Controller (Consumer Device).
* **Endpoint Interrupts:** Timing and data packet structure of USB interrupt transfers.
* **State Machine:** Button debounce and management of USB connection states (Suspend/Resume).

## 🛠 Hardware and Software
* **MCU:** STM32F103 (BluePill) / STM32F4 Series
* **Interface:** USB 2.0 Full Speed (12 Mbit/s)
* **Class:** Human Interface Device (HID) - No Driver Required

## 🚀 How Does It Work?
When connected to a computer, the device identifies itself as a “Multimedia Keyboard”. When the defined GPIO pins (Buttons) are pressed, the corresponding USB HID report (e.g., `0xEA` - Volume Down) is sent to the operating system. It works as plug-and-play on Windows, Linux, and macOS.

---
*Adapted from open-source HID implementations for embedded systems study purposes.* 


