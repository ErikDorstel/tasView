# tasView
simple javascript web UI to manage Tasmota IoT devices via mqtt websocket protocol
#### Features
* zero touch auto discovery of tasmota devices
* control up to 4 power switches per device
* display up to 4 switch inputs per device
* display up to 4 analog inputs per device
* display energy monitor values with auto scale
* display environment monitor values of connected sensors
* optional logging display
#### Auto Discovery
The auto discovery function evaluates LWT (last will testament) messages and uses status commands to query the properties of the Tamota devices.
#### MQTT client web socket library
The following library is required for MQTT websocket communication and must be placed in the same directory as the tasView html page.
https://github.com/hivemq/hivemq-mqtt-web-client/blob/master/js/mqttws31.js
#### Screenshot
![IMAGE ALT TEXT HERE](http://www.dorstel.de/github/tasView1.png)
