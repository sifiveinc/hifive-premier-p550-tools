# EsMacIdUpdateTool User Manual

## Introduction

The **EsMacIdUpdateTool** is a utility designed to run on windows to update the three MAC addresses on our development board. Every time a target development board is detected, the tool will automatically update the MAC addresses of the board. 

Once the operations are finished, the program will exit. To update the MAC addresses again, the program needs to be manually executed once more.

If multiple target development boards are connected to your computer, our program will update all the detected target development boards. 

## System Requirements

- **Operating System**: Windows 64-bit

## Prerequisites

Before running the tool, ensure that the MCU (Microcontroller Unit) of the development board is powered on. If the MCU is not powered on, the tool will fail to detect the development board. This step is crucial to avoid detection failure and ensure proper functionality of the tool.

Additionally, make sure that the serial port is not being used by any other program. If the serial port is occupied, the update process will fail.

## Usage

### Run the Tool
- To start the tool on Windows, you can either:
   - Open **Command Prompt** or **PowerShell** and run the following command:
     ```bash
     .\EsMacIdUpdateTool.exe
     ```
   - Or simply **double-click** the `EsMacIdUpdateTool.exe` executable to run it.

### MAC Address Update

- The tool will detect the target development board and automatically update the three MAC addresses.

### Completion

- After the update process is finished, the tool will exit automatically.

### Re-running the Tool

- To update the MAC addresses again, you must run the program manually once again.

### Successful Update Output

- If the update is successful, you will see the following complete output:
   ```bash
    =============================================================
    New device detected, serial port is:  "COM15"
    Serial port "COM15" opened successfully
    MAC IDs for SN  "SF106SKB245000xxxx" : "8C:1F:xx:xx:xx:xx" "8C:1F:xx:xx:xx:xx" "8C:1F:xx:xx:xx:xx"
    UPDATE MAC ADDRESS SUCCESS FOR SN: "SF106SKB245000xxxx"
    =============================================================
   ```
