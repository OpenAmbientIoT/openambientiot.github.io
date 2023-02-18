# MQTT


## Overview

MQTT (Message Queue Telemetry Transport) is a publish/subscribe-based messaging protocol that is widely used for IoT (Internet of Things) 
and M2M (Machine to Machine) communications. It is designed to be lightweight and efficient, 
making it well-suited for resource-constrained devices such as sensors and embedded systems.

## How MQTT works?

### Topics

In MQTT, messages are categorized and sent to specific "topics." Subscribers can filter the messages they receive based 
on the topics they are interested in.

### Publish/Subscribe

There are two types of entities in MQTT: publishers and subscribers. Publishers send messages to a topic, and subscribers 
receive messages sent to the topics they are interested in.

### Broker

The broker is a server that acts as the central point of communication. It manages the distribution of messages between 
publishers and subscribers by receiving messages from publishers, filtering them based on topics, and sending the 
filtered messages to interested subscribers.

### Quality of Service (QoS)

MQTT supports three levels of QoS to determine the reliability of message delivery. 
The three levels are: 
- QoS 0 (at most once)
- QoS 1 (at least once)
- QoS 2 (exactly once).

### Connection and Disconnection 

MQTT devices can connect and disconnect from the broker at any time. The broker maintains the state of the devices and 
allows them to receive messages even if they were disconnected and then reconnected later.

### Keep Alive

MQTT devices send periodic "keep alive" messages to the broker to indicate that they are still connected. 
This helps the broker detect lost connections and remove inactive devices.

MQTT is a simple and efficient method for IoT devices to communicate with servers and with each other, 
making it a popular choice for IoT and M2M communication.
