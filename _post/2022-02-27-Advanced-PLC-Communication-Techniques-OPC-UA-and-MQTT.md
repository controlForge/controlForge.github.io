---
title: "Advanced PLC Communication Techniques: OPC UA and MQTT" 
date: 2022-02-27 11:42:38 +0000
categories: [Article]
tags: []     # TAG names should always be lowercase
---


## Introduction

In modern industrial automation systems, effective communication between programmable logic controllers (PLCs) plays a crucial role. Traditional communication methods have limitations in terms of scalability, security, and interoperability. This article explores advanced communication techniques in PLC systems, focusing on OPC UA (Unified Architecture) and MQTT (Message Queuing Telemetry Transport). We will provide step-by-step tutorials on setting up communication channels and exchanging data using these protocols.


## 1. OPC UA: An Overview

### Introduction to OPC UA

OPC UA (Unified Architecture) is an industrial communication protocol that provides a platform-independent, scalable, and secure framework for exchanging data between different devices in a network. It offers a standardized way of representing data, services, and events, ensuring interoperability between various systems.

### Key Features and Benefits

- Platform independence: OPC UA is designed to work on different operating systems and hardware platforms, enabling seamless integration across heterogeneous systems.
- Scalability: OPC UA supports both small-scale and large-scale systems, allowing for the inclusion of thousands of devices and millions of data points.
- Security: OPC UA incorporates robust security mechanisms, including encryption, authentication, and access control, to protect data integrity and prevent unauthorized access.
- Extensibility: OPC UA provides a flexible data model that allows for the representation of complex data structures, making it suitable for diverse industrial applications.
- Pub/Sub Model: OPC UA supports a Publish-Subscribe communication model, enabling efficient data distribution across multiple subscribers.

## 2. MQTT: An Overview

### Introduction to MQTT

MQTT (Message Queuing Telemetry Transport) is a lightweight publish-subscribe messaging protocol designed for constrained devices and low-bandwidth, high-latency networks. It is widely used in IoT (Internet of Things) and industrial applications where bandwidth and resources are limited.

### Key Features and Benefits

- Lightweight: MQTT is designed to be efficient and consume minimal network bandwidth, making it suitable for low-power devices and networks with limited resources.
- Publish-Subscribe Model: MQTT follows a publish-subscribe communication pattern, allowing multiple subscribers to receive data from publishers without direct point-to-point connections.
- Quality of Service (QoS): MQTT supports different levels of QoS to ensure reliable message delivery, even in unreliable network conditions.
- Asynchronous Communication: MQTT enables asynchronous messaging, allowing devices to send and receive data independently without requiring constant connections.
- Wide Protocol Support: MQTT is supported by various programming languages and platforms, making it highly interoperable and easy to integrate into existing systems.

## 3. Setting Up OPC UA Communication

### Installing OPC UA Server Software

To set up OPC UA communication, the first step is to install an OPC UA server software on the machine that will act as the server. Several commercial and open-source OPC UA server implementations are available, such as KEPServerEX. Choose a suitable OPC UA server software based on your requirements and install it following the provided instructions.

### Configuring OPC UA Server

Once the OPC UA server software is installed, it needs to be configured to communicate with the PLC. The configuration process may vary depending on the specific server software chosen. Generally, the steps involve:

1. Launching the OPC UA server configuration tool.
2. Creating a new server project or configurationfile.
3. Specifying the PLC connection settings, such as the PLC model, communication protocol, and connection parameters.
4. Configuring security settings, including certificates, encryption, and authentication mechanisms.
5. Defining OPC UA data tags and their corresponding PLC addresses or variables.

Refer to the user manual or documentation of your OPC UA server software for detailed instructions on configuring the server.

### Setting Up OPC UA Client

To establish communication with the OPC UA server, an OPC UA client software needs to be set up. The OPC UA client can run on the same machine as the server or on a separate device connected to the network.

1. Install an OPC UA client software that is compatible with your OPC UA server.
2. Launch the OPC UA client software and create a new client project or configuration file.
3. Specify the server connection details, including the server address, port number, and security settings.
4. Establish a connection with the OPC UA server and authenticate if required.

Again, consult the documentation or user manual of your OPC UA client software for specific instructions on setting up the client.

### Establishing Communication Channels

Once the OPC UA server and client are configured and connected, you can establish communication channels to exchange data between the PLC and the client.

1. In the OPC UA client software, browse the OPC UA server's address space to discover the available data tags or variables.
2. Select the desired data tags or variables that you want to read from or write to the PLC.
3. Configure read and write operations for the selected data tags.
4. Test the communication channels by performing read and write operations to verify successful data exchange.

## 4. Exchanging Data with OPC UA

### Defining OPC UA Data Tags

Before exchanging data with the PLC using OPC UA, it is essential to define OPC UA data tags that correspond to the PLC data points or variables.

1. In the OPC UA server configuration, create OPC UA data tags based on the PLC's data structure.
2. Assign OPC UA node IDs or addresses to the data tags, ensuring they match the PLC addresses or variables.

### Reading Data from PLC using OPC UA

To read data from the PLC using OPC UA, follow these steps:

1. In the OPC UA client software, browse the OPC UA server's address space to locate the desired data tags.
2. Select the data tags or variables from which you want to read data.
3. Configure read operations for the selected data tags, specifying the desired read frequency or trigger conditions.
4. Initiate the read operation and retrieve the data from the PLC.

### Writing Data to PLC using OPC UA

To write data to the PLC using OPC UA, follow these steps:

1. In the OPC UA client software, browse the OPC UA server's address space to find the desired data tags.
2. Select the data tags or variables to which you want to write data.
3. Configure write operations for the selected data tags, specifying the desired write frequency or trigger conditions.
4. Provide the data values to be written to the PLC and initiate the write operation.

### Subscribing to Data Changes

OPC UA supports data subscriptions, allowing the OPC UA client to receive notifications when the subscribed data changes. To subscribe to data changes from the PLC:

1. In the OPC UA client software, select the data tags or variables for which you want to receive notifications.
2. Configure the subscription settings, including the sampling rate and notification conditions.
3. Establish the data subscription with the OPC UA server.
4. Monitor the subscribed data for changes and handle the received notifications accordingly.

## 5. Setting Up MQTT Communication

### Installing MQTT Broker

To set up MQTT communication, an MQTT broker (also known as a message broker) needs to be installed. An MQTT broker is responsible for receiving messages from publishers and delivering them to subscribers. Popular MQTT broker implementations include EMQX. Choose an MQTT broker software that suits your requirements and install it following the provided instructions.

### Configuring MQTT Broker

Once the MQTT broker software is installed, it needs to be configured to enable communication with the PLC and MQTT clients.

1. Launch the MQTT broker configuration tool or edit the configuration file directly.
2. Specify the broker settings, such as the network interface, port number, and security options.
3. Configure authentication and access control mechanisms if required.
4. Define topics or topic hierarchies to categorize the MQTT messages.
5. Set up connection limits, quality of service (QoS) options, and other advanced settings as needed.

Refer to the documentation or user manual of your chosen MQTT broker software for detailed instructions on configuring the broker.

### Setting Up MQTT Client

To establish communication with the MQTT broker, an MQTT client software or library needs to be set up. The MQTT client can run on the same machine as the broker or on separate devices connected to the network.

1. Install an MQTT client software or library compatible with your programming language or platform.
2. Configure the MQTT client with the broker connection details, including the broker address
, port number, and security settings.
3. Establish a connection with the MQTT broker using the configured client.
4. Authenticate the MQTT client if required by the broker.

Again, consult the documentation or user manual of your chosen MQTT client software or library for specific instructions on setting up the client.

### Establishing Communication Channels

Once the MQTT broker and client are set up and connected, you can establish communication channels to exchange data between the PLC and MQTT clients.

1. In the MQTT client software or library, publish messages to specific MQTT topics to send data to the broker.
2. Subscribe to MQTT topics of interest to receive data published by other MQTT clients or the PLC.
3. Specify the desired quality of service (QoS) level for both publishing and subscribing, considering the reliability and bandwidth constraints of your network.
4. Handle incoming messages from subscribed topics and process the received data accordingly.

## 6. Exchanging Data with MQTT

### Defining MQTT Topics

Before exchanging data with the PLC using MQTT, it is necessary to define MQTT topics that represent the different data points or variables.

1. Determine the data structure and organization of the PLC data that you want to exchange via MQTT.
2. Design a topic hierarchy that reflects the logical grouping of the data points.
3. Assign unique topic names to each data point or variable, ensuring they follow a consistent naming convention.

### Publishing Data to MQTT Broker

To publish data to the MQTT broker from the PLC or MQTT clients, follow these steps:

1. Determine the data to be published and its corresponding MQTT topic.
2. Format the data according to the desired payload format, such as JSON or binary.
3. Use the MQTT client software or library to publish the data to the specified MQTT topic.
4. Specify the desired QoS level for the published message, considering the reliability requirements.

### Subscribing to MQTT Topics and Receiving Data

To receive data from the PLC or other MQTT clients, follow these steps:

1. Identify the MQTT topics of interest that you want to subscribe to.
2. Use the MQTT client software or library to subscribe to the desired MQTT topics.
3. Specify the desired QoS level for the subscribed topics, considering the reliability and bandwidth constraints.
4. Handle incoming messages from the subscribed topics in your application or system, extracting and processing the received data.

### Quality of Service (QoS) Considerations

When exchanging data using MQTT, it is essential to consider the appropriate quality of service (QoS) level for each message.

1. QoS 0 (At most once): This level offers the lowest reliability, where messages are delivered at most once. There is no guarantee of message delivery, and no acknowledgment or retry mechanism is employed.
2. QoS 1 (At least once): This level ensures message delivery at least once. The broker acknowledges the receipt of the message and attempts to deliver it to subscribers. Retransmission is performed until the acknowledgment is received.
3. QoS 2 (Exactly once): This level provides the highest reliability, guaranteeing that messages are delivered exactly once. It involves a four-step handshake process to ensure message integrity and reliability.

Choose the appropriate QoS level based on the criticality and reliability requirements of your data exchange.

## 7. Integrating OPC UA and MQTT

To leverage the strengths of both OPC UA and MQTT, it is possible to integrate them, enabling bi-directional data exchange and interoperability between systems.

### Mapping OPC UA Tags to MQTT Topics

When integrating OPC UA and MQTT, it is necessary to establish a mapping between OPC UA data tags and MQTT topics. This mapping allows data from the PLC, represented by OPC UA tags, to be published to MQTT topics and vice versa.

1. Define a mapping scheme that associates OPC UA tags with MQTT topics.
2. Establish rules or conventions for naming and structuring the MQTT topics to align with the OPC UA tags.
3. Create a mapping table or configuration that links OPC UA tags to their corresponding MQTT topics.
4. Ensure the mapping is synchronized and consistently applied across the OPC UA server, MQTT broker, and client applications.

### Bridging OPC UA and MQTT using Gateway Software

To bridge the communication between OPC UA and MQTT, gateway software or middleware can be employed. This software acts as an intermediary, translating data between the OPC UA and MQTT protocols.

1. Select a suitable OPC UA-to-MQTT gateway software that provides the necessary functionalities.
2. Install and configure the gateway software, specifying the OPC UA server and MQTT broker connection details.
3. Set up the mapping between OPC UA tags and MQTT topics within the gateway software.
4. Enable data exchange between OPC UA and MQTT by establishing connections with the OPC UA server and MQTT broker.
5. Monitor and manage the data flow between OPC UA and MQTT to ensure reliable and efficient communication.

### Implementing Bi-Directional Data Exchange

With the OPC UA and MQTT integration in place, bi-directional data exchange between the PLC and other systems becomes possible.

1. Data from the PLC is read using OPC UA andpublished to MQTT topics through the OPC UA-to-MQTT gateway.
2. MQTT clients or other systems subscribe to the MQTT topics to receive the published data.
3. MQTT clients can also publish data to specific MQTT topics, which is then received by the OPC UA-to-MQTT gateway.
4. The gateway translates the MQTT messages into OPC UA data and writes it to the corresponding OPC UA tags, allowing other systems to access the data through OPC UA.

This bi-directional data exchange enables seamless interoperability between OPC UA and MQTT, facilitating the integration of the PLC with a wide range of systems and applications.

## 8. Securing MQTT Communication

When implementing MQTT communication for the PLC, it is crucial to ensure the security of the data exchange. MQTT provides various security features that can be employed to protect the confidentiality, integrity, and authenticity of the transmitted data.

### Transport Layer Security (TLS) Encryption

Using Transport Layer Security (TLS) encryption ensures that the MQTT communication is encrypted, preventing unauthorized access or tampering of the data. TLS protects the data in transit by establishing secure connections between the MQTT client and broker.

To enable TLS encryption:

1. Obtain a TLS certificate from a trusted certificate authority (CA) for the MQTT broker.
2. Configure the MQTT broker to use the TLS certificate and enable TLS encryption.
3. Configure the MQTT client to use TLS encryption and provide the necessary certificate information.

By enabling TLS encryption, you can establish a secure communication channel between the PLC and MQTT clients.

### Authentication and Access Control

To ensure that only authorized entities can access the MQTT broker and exchange data:

1. Enable authentication on the MQTT broker, requiring clients to provide valid credentials.
2. Configure the MQTT clients to authenticate themselves with the broker using appropriate credentials.
3. Implement access control policies on the MQTT broker to restrict access to specific topics or actions based on client credentials.

Authentication and access control mechanisms help prevent unauthorized access and protect the data exchanged through MQTT.

### Message Payload Encryption

In scenarios where the payload of MQTT messages contains sensitive or confidential data, it is advisable to encrypt the message payload itself. This ensures that even if the communication is intercepted, the data remains encrypted and cannot be understood.

To encrypt the message payload:

1. Implement message payload encryption within the MQTT client software or library.
2. Use a secure encryption algorithm and key management mechanism to encrypt and decrypt the payload data.

By encrypting the message payload, you add an extra layer of security to the MQTT communication, safeguarding the confidentiality of the data.

### Secure MQTT Broker Configuration

In addition to the encryption and authentication measures mentioned above, consider implementing the following security practices for the MQTT broker:

1. Regularly update the MQTT broker software to ensure you have the latest security patches and bug fixes.
2. Disable unnecessary features or protocols that are not required for your specific use case.
3. Configure secure default settings for the MQTT broker, such as strong passwords and limited access rights.
4. Monitor and log MQTT communication for potential security threats or anomalies.

By following these security practices, you can enhance the overall security of the MQTT communication and protect the integrity and confidentiality of the data exchanged.

## Conclusion

Integrating a PLC with MQTT communication opens up new possibilities for connecting industrial systems with the broader IoT ecosystem. MQTT's lightweight and publish-subscribe architecture, combined with OPC UA's robust data modeling and interoperability capabilities, provide a powerful solution for exchanging data between the PLC and other systems.

By following the steps outlined in this article, you can successfully implement MQTT communication for your PLC, establish communication channels, exchange data, and ensure the security of the MQTT communication.

Remember to refer to the documentation and user manuals of your specific PLC, MQTT client software, and OPC UA server for detailed instructions and guidelines tailored to your setup. With careful planning and implementation, you can harness the power of MQTT to enable efficient and seamless integration of your PLC into the IoT landscape.