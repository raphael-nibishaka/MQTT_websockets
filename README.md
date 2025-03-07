# MQTT Weather Station (WebSockets)

A simple weather station interface that displays real-time temperature and humidity data by connecting to an MQTT broker over WebSockets.

## Features
- **Real-Time Data**: Displays the temperature and humidity in real-time using MQTT messages.
- **MQTT WebSocket Connection**: Uses the MQTT protocol over WebSockets to subscribe to temperature and humidity data.
- **Simple UI**: A clean and minimal design to display the temperature and humidity data.

## Project Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/raphael-nibishaka/MQTT_websockets.git
Open the index.html file in a browser to view the weather station interface.
Technologies Used
HTML: For the structure of the page.
CSS: For the styling of the weather station.
JavaScript: For the logic of connecting to the MQTT broker and displaying data.
MQTT.js: A library for connecting to an MQTT broker via WebSockets.
MQTT Broker
The application connects to an MQTT broker at ws://157.173.101.159:9001 to receive temperature and humidity data. You can change the broker URL if necessary.

Subscribed Topics
The application subscribes to the following MQTT topics to receive data:

Temperature: /work_group_01/room_temp/temperature
This topic provides the temperature data.

Humidity: /work_group_01/room_temp/humidity
This topic provides the humidity data.

How It Works
MQTT Connection: The page connects to the MQTT broker over WebSockets at the specified URL (ws://157.173.101.159:9001).
Subscribing to Topics: Upon connection, the page subscribes to two MQTT topics:
/work_group_01/room_temp/temperature for temperature data.
/work_group_01/room_temp/humidity for humidity data.
Receiving Data: When a new message is received on either of these topics, the temperature and humidity values are extracted from the message payload.
Displaying Data: The received temperature and humidity data are displayed on the webpage in real-time.
MQTT Message Flow
The client (weather station) listens for messages published to the subscribed topics.
When a message is received, it updates the displayed data on the page, ensuring that the weather station shows the latest information.
License
This project is open-source and available under the MIT License.
