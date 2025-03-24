# EsMacIdUpdateTool User Manual

## Introduction

The **EsMacIdUpdateTool.run** is a utility designed to run on MacOS systems to update the three MAC addresses on our development board. Every time a target development board is detected, the tool will automatically update the MAC addresses of the board.

Once the operations are finished, the program will exit. To update the MAC addresses again, the program needs to be manually executed once more.

If multiple target development boards are connected to your computer, our program will only update all the detected target development boards.

## System Requirements

- **Operating System**: MacOS 12.* and M1 chip later

## Prerequisites

Before running the tool, make sure the MCU of the development board is powered on. Failing to do so may result in detection failure. This is a crucial step before connecting to the board.

Additionally, make sure that the serial port is not being used by any other program. If the serial port is occupied, the update process will fail.

## Usage

### Run the Tool
- To start the tool, simply run the following command:
   ```bash
   sudo ./EsMacIdUpdateTool.run
   ```

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
### Note
 - Please execute command "/usr/sbin/softwareupdate --install-rosetta --agree-to-license" if you encounter "bad cpu type in executable" error when running this tool
