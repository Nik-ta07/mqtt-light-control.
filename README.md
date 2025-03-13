MQTT Light Control Project

📌 Overview

This is a simple web-based application that allows users to switch a light ON or OFF over MQTT. It also includes a Python script that simulates an ESP8266 IoT device, which listens for the MQTT messages and prints whether the light is ON or OFF.

📂 Project Structure

/mqtt-light-control
│── index.html          # Web interface for sending MQTT commands
│── light_simulation.py # Python script simulating the IoT device
│── README.md           # Project documentation

🚀 Features

Web interface with ON/OFF buttons.

Uses MQTT.js to publish messages over MQTT.

Python script that listens for MQTT messages and prints light status.

Hosted using Mosquitto's public MQTT broker.

🌍 Web Interface (index.html)

The webpage allows users to send MQTT messages by clicking buttons:

Turn ON → Publishes "ON" to the MQTT topic.

Turn OFF → Publishes "OFF" to the MQTT topic.

Displays the last sent command.

🛠 Simulated IoT Device (light_simulation.py)

The Python script simulates an ESP8266 by:

Subscribing to /student_group/light_control.

Printing "💡 Light is TURNED ON" if it receives "ON".

Printing "💡 Light is TURNED OFF" if it receives "OFF".

🔧 Setup & Run

1️⃣ Run the Python MQTT Listener

pip install paho-mqtt
python light_simulation.py

2️⃣ Open Web Interface

Open index.html in a web browser.

Click Turn ON / Turn OFF.

Check the Python script output.

📡 MQTT Broker

Broker: test.mosquitto.org

Topic: /student_group/light_control

