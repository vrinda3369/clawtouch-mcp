# 🖱️ clawtouch-mcp - Control your computer using AI agents

[![Download clawtouch-mcp](https://img.shields.io/badge/Download-clawtouch--mcp-blue.svg)](https://github.com/vrinda3369/clawtouch-mcp)

This tool connects your AI accounts to your computer hardware. It allows AI models to move your mouse and type on your keyboard. It uses a Raspberry Pi Pico 2 to act as a physical device that your computer recognizes as a standard mouse and keyboard. Your AI agent gains the ability to interact with your screen and apps just like a human.

## 📋 What this tool does

The clawtouch-mcp server bridges the gap between digital AI assistants and your physical workspace. Modern AI models can reason and plan, but they often lack the ability to click buttons or enter text into your desktop applications. This software bridges that gap. By using the Model Context Protocol, the tool translates instructions from your AI agent into physical signals.

Your computer sees a legitimate USB device. It does not know the input comes from an AI model. This setup allows for automation of tasks that normally require a human user. You can automate data entry, file management, or complex desktop workflows without constant supervision.

## ⚙️ Hardware requirements

To use this software, you need specific hardware. Ensure you have the following items ready:

* A Raspberry Pi Pico 2 or a compatible RP2350 microcontroller board.
* A high-quality USB-A to Micro-USB or USB-C cable, depending on your board type.
* A spare USB port on your Windows computer.

The Raspberry Pi Pico 2 acts as the physical bridge. It receives commands from your computer over the USB connection and relays them to your operating system as standard HID events. This ensures compatibility with Windows, macOS, and Linux without needing additional drivers.

## 🚀 Getting started

Follow these steps to set up your system for the first time.

1.  **Download the software.** Visit the [official releases page](https://github.com/vrinda3369/clawtouch-mcp) to download the latest version for Windows.
2.  **Connect your hardware.** Plug the Raspberry Pi Pico 2 into a USB port on your machine. Wait for Windows to identify the hardware.
3.  **Run the installer.** Open the file you downloaded. Follow the prompts on your screen to install the server application.
4.  **Launch the app.** Open the clawtouch-mcp program from your Start menu once the installation finishes.

## 📥 Downloading and setup

You must visit the project website to acquire the necessary files. 

[Visit the clawtouch-mcp repository link to download](https://github.com/vrinda3369/clawtouch-mcp)

Confirm the download completes before you start the installation. If Windows displays a security prompt, click "More info" and then "Run anyway" to proceed. This is standard for new software downloads.

The installer will configure the connection between your AI agent and the hardware. It will scan for your Raspberry Pi Pico 2 automatically. You should see a notification on your screen confirming that the hardware is ready for use. If the device does not appear, disconnect the cable and try a different USB port on your machine.

## 🤖 Using the AI integration

Once the server runs, you must connect it to your preferred AI agent environment. This usually involves adding the server address to your AI model configuration file. Most agents use a local address such as `http://localhost:8080`. 

When your agent connects, it gains access to specific tools. These tools include:

* **Move mouse:** Sets the cursor to specific screen coordinates.
* **Click:** Performs left, right, or double clicks.
* **Type:** Inputs text at the cursor position.
* **Drag and drop:** Performs complex mouse movements for file management.

Your AI model will request permission before taking control of your hardware if your agent interface includes security settings. Monitor the logs in the clawtouch-mcp window to track the actions executed by the agent.

## 🛠️ Troubleshooting common issues

If you encounter difficulties, review these common solutions:

* **The device is not detected:** Ensure you use a data-capable USB cable. Some cables only provide power and cannot transmit data. Check that the LED on your Raspberry Pi Pico 2 lights up.
* **The agent refuses to connect:** Check that the clawtouch-mcp server is currently open. Ensure your firewall allows the server application to communicate on local ports.
* **Inaccurate movements:** Sometimes screen scaling settings in Windows interfere with pixel tracking. Ensure your display scale is set to 100% if the cursor misses targets.
* **Sluggish response:** Close unnecessary browser tabs or background processes. AI agents can consume significant memory during complex tasks.

## 🔒 Security and privacy

The clawtouch-mcp server runs entirely on your local machine. It does not send your screen data or keystrokes to a cloud server. Only you and the AI agent you explicitly authorize have control over your hardware. 

To maintain security, never leave your computer unattended while the AI agent has active control. Close the clawtouch-mcp application when you finish your work tasks to cut the link between your hardware and your software agents.

## 📈 Advanced configuration

You can refine how the tool behaves by editing the configuration file. This file usually resides in the installation folder. You can adjust the speed of mouse movements, the delay between keystrokes to prevent input errors, and the specific connection ports.

Consult the documentation within the application folder for a list of available settings. Modifying these values helps if you run applications that require slow, specific input sequences to function correctly. 

## 📝 Final check

Ensure your operating system is up to date before installing the software. Windows 10 or 11 provides the best support for HID devices. If you use a virtual machine, ensure that the USB device correctly passes through to the guest operating system.

By maintaining a clear path for data between the agent and your hardware, you ensure consistent performance. Your clawtouch-mcp setup will serve as a stable foundation for all your automation experiments and productivity workflows.