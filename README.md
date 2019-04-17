# gcloud IoT Tutorial
A very simple Tutorial to connect an IoT Device to gcloud over MQTT.
This tutorial is part of the a course for mechanical engineers to get familiar with the cloud side of the IoT stack.

## Intial Situation
* Studneds have developed a simple machine that sorts Lego bricks. The machine has sensor(s) to control it success/failure rate in picking and placing the bricks to the corect position (Machine is built with Lego and Arduino).
* The embedded software on the machine is able communicate with Raspberry PI via a proprietary protocol (Textmessages over BLE).
* The Raspberry Pi acts as a gateway between the factory where machine is operating and the cloud where the success/failure rates of all machins are tracked by the producer of the machine to further improve it.
* Node-red is running on the Raspberry Pi

## Goals of the Tutorial

Overall Goal: 
* Connect Node-red to gCloud over MQTT and store success/failure statistics of a device
* Get familiar with cloud plattforms
* Get familier with basic device management
* Get faimliar with basic security/authenitcation concepts

Steps to be done
* Open an account on gCloud
* Create a virtual device on IoT Core
* Connect the real device to IoT Core
* Act on incomming data of devices
* Store the incomming data into a database 
* Vizualize data

## Step by step tutorial

### Open an Account on gCloud
1. Create an Account for Google cloud, using your voucher.
2. Login to the console and make sure you are working in the correct project

### Setup of IoT Core
1. On the left navigation bar select IoT Core (its located in the "Big Data" section
2. Activate the IoT Core service
3. Create a regisitry. The regisitry groups together a fleet of devices that share common properties and rules e.g. for a particular application.
```
Name: pde-pickandplace-modules
Region: europe-west1
Protocol: MQTT and HTPP
Default telemetry topic: Create new topic 'default'
Device state topic: Create new topic 'status'
Stackdriver Logging: None
```

### Setup of Device (Node-Red)


## Vizalize Data
