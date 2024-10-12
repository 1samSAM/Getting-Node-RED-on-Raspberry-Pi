# Getting-Node-RED-on-Raspberry-Pi
Node-RED is a flow-based development tool for visual programming, ideal for IoT projects. This guide walks through the steps to install Node-RED on a Raspberry Pi.

## Prerequisites

- Raspberry Pi (Raspberry Pi 3 or 4 recommended)
- Raspbian OS (Lite or Full, updated)
- Internet connection
- Monitor, keyboard, mouse, or SSH access

## Step 1: Update your Raspberry Pi

Update your system's package list and upgrade existing packages:

```bash
sudo apt update
sudo apt upgrade
```
##Step 2: Install Node-RED

Use the Node-RED team's installation script to install Node.js and Node-RED:

```bash
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
```
The script will:

Install Node.js
Install Node-RED
Optionally install useful tools
Follow the prompts during installation.

##Step 3: Set Node-RED to Start on Boot
To enable Node-RED to start automatically on boot, run:

```bash
sudo systemctl enable nodered.service
```
To manually start Node-RED:
```bash
node-red-start
```
To stop Node-RED:
```bash
node-red-stop
```
To check the Node-RED service log:
```bash
Copy code
node-red-log
```
##Step 4: Access the Node-RED Interface
Once Node-RED is running, access the flow editor by opening a browser and navigating to:

plaintext
```http://<your-pi-ip-address>:1880```
If you're working locally on the Raspberry Pi:
plaintext
```http://localhost:1880```
##Step 5: Start Creating Flows
Node-RED is now up and running. Start creating flows by dragging nodes and wiring them together.
Additional Resources
Node-RED Documentation
Node-RED Flows Library
