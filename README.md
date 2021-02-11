# tasView
simple javascript web UI to manage Tasmota IoT devices via mqtt websocket protocol
#### Features
* zero touch auto discovery of tasmota devices
* control up to 4 power switches per device
* display up to 4 switch inputs per device
* display up to 4 analog inputs per device
* display energy monitor values with auto scale
* display environment monitor values of connected sensors
* automatic zoom factor adjustment to fit small displays
* optional logging textbox
* optional CLI console to send commands to one or some or all connected tasmota devices
#### Auto Discovery
The auto discovery function trigger on LWT (last will testament) messages and uses Tasmota mqtt status commands to query the properties of the Tasmota devices.
#### MQTT client websocket library
The following javascript library is required for mqtt websocket communication and must be placed in the same directory as the tasView html page.
https://github.com/hivemq/hivemq-mqtt-web-client/blob/master/js/mqttws31.js
#### MQTT broker
tasView requires a websocket enabled mqtt broker. The hostname of the mqtt broker and the websocket tcp port can be configured in the tasView javascript source. If the mqtt broker runs on the same host as the web server and the websocket port is 9001, no changes are needed.
#### CLI Console
The commands consist of three parts which are separated by spaces.
* topic filter (* for all devices, a part of or a full device name, a regular expression)
* command name (like status or timezone ...)
* command payload (optional)
#### tasView installation
To install tasView on an unix based web server e.g. apache, copy install.sh to a web server folder and follow the steps below.
* chmod 744 install.sh
* ./install.sh
#### mosquitto installation
To install the mqtt broker mosquitto on an unix based host follow the steps below.
* sudo apt get mosquitto
* modify the configuration file /etc/mosquitto/mosquitto.conf as published in the repository
* sudo systemctl stop mosquitto.service
* sudo systemctl start mosquitto.service
#### Screenshot
![IMAGE ALT TEXT HERE](https://www.dorstel.de/github/tasView.png?)
