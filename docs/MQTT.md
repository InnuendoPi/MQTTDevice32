# MQTT

MQTT is a publish-and-subscribe protocol. Clients, devices and applications publish and subscribe into topics handled by a broker. In a CraftbeerPi environment a sensor is a publishing and an actor is a subscribing device. Devices or applications never communicate directly, instead they send and receive messages managed in topics by the MQTT broker. A topic looks like a named channel or folder, eg induction/temp or upstairs/bathroom/light. Hundreds of different topics are possible. Each topic behave like a message in- and outbox. Messages are send in a compact JSON format, also known as payloads. A simple payload from a sensor device can look like this: { "value": 21.2 }. The sensor publishes this message into a topic. All subscribed clients, devices or application to this topic will receive the sensor message "value 21.2". A simple payload from CraftbeerPi to an actor can be { "state": "on"}. CBPi4 publishes this message into a topic to switch on an actor. An actor must subcribe to this topics to receive this message.

MQTT summary:

* sensors are publishing payloads (sensor values) into topics
* actors subscribe to topics to receive payloads (commands)
* every published payload will always be sent to a MQTT broker
* the MQTT broker sends every received payload to all subscribing devices and applications
* craftbeerpi subscribes to all sensor topics and publishes actor commands in actor topics
* all sensor and actor topics are unique
