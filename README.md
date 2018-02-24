ESP01/s (ESP8266) has embedded WIFI add faster processor  which can connect with an Arduino board to get more sensor extensibility.

However , there is a common problem  
Some of Arduino  only contains one serial port for usb connection. so only soft serial can be used to connect with ESP8266. In this case since the Arduino perform the loop much faster than soft serial communication speed, lots of MQTT message will be lost and we have to use delay in the loop to wait for MQTT message. 

the library will sovle the problem to make ESP01/s as independent MQTT node. it make ESP01/s take full responsibility to communicate with MQTT server and parse the command on both way.
