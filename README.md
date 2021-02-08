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
#### Auto Discovery
The auto discovery function trigger on LWT (last will testament) messages and uses Tasmota mqtt status commands to query the properties of the Tasmota devices.
#### MQTT client websocket library
The following javascript library is required for mqtt websocket communication and must be placed in the same directory as the tasView html page.
https://github.com/hivemq/hivemq-mqtt-web-client/blob/master/js/mqttws31.js
#### MQTT broker
tasView requires a websocket enabled mqtt broker. The hostname of the mqtt broker and the websocket tcp port can be configured in the tasView javascript source.
#### Screenshot
![IMAGE ALT TEXT HERE](http://www.dorstel.de/github/tasView.png)
