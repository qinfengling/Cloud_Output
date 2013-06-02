
Introduction
===========================
Overview of Dragino
------------------------
Node is a platform for IoT. It reads physical data from the Sensor and accomplishes certain actions via the Actuator. A Sensor is an electronic object that gets physical values from the environment. For instance, a Grove-Temperature Sensor reads temperature data and transports it to Beacon. An Actuator makes some certain actions. As an example, Grove-LED will blink when a HIGH level is sent to it.

Node is found by two parts, Atom and Cloud. You can use a Cloud to send data to Yeelink, Xively etc. 

Dragino MS12 is an open source, Wi-Fi/Linux enable appliance for MCU project. The goal of the Dragino is to solve the connectivity problem and greatly enhance microcontroller products such as the Arduino. Dragino MS12 is motherboard base and it normally need to work with different kind of plug-in daughter boards for different projects.

Dragino in an IoT project
------------------------

![github](https://dl.dropboxusercontent.com/u/88978125/dragino_cloud.jpg "github")
Note: The daughter is a separate part from MS12, a reference can be found on dragrove 


Above is a structure to show how to use Dragino MS12 to develop IOT products. In this structure, there are three main parts:

* IoT Server: they are servers which store data from the sensor and process these data in its manner (for example plotting the data for easy reading). IoT servers are not subject in monitoring; they may also send commands to control the sensors. 
A public server example is www.xively.com (formally pachube or cosm)
* Gateway: Sensors normally can’t communicate to IoT servers directly. They need a gateway. Here MS12 plus a daughter board acts as a gateway, the daughter board get data from sensors and send it to MS12, MS12 then send the data to IoT server via TCP/IP protocol.
* Nodes: sensors or controllers

Dragino has developed a firmware for IoT (Internet of Things) applications. The firmware can be found on this link: http://wiki.dragino.com/index.php?title=Release_Note 

Features of the IoT firmware
----------------------------
1.  Completely Open Source.
2.	RESTful server compatibility 
  *	Compatible with Yeelink, xively RESTful server
  * tomatically create nodes in RESTful server
  * Automatically update sensor data to RESTful server
  * Automatically delete nodes from RESTful server
3.	Support custom commands to process sensor data
4.	Support record data to local server
5.	Support internet connection via Wi-Fi or LAN port.
6.	Support DDNS (Dynamic DNS) service
7.	Support Firmware Upgrade via Web GUI
