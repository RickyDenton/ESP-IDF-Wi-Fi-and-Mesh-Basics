# ESP-IDF Mesh Stack Application Framework & Practical Guide

The purpose of this program is to provide a comprehensive framework for developing applications using the mesh networking features currently offered by the ESP-IDF mesh stack as of version 3.1, where a comprehensive analysis of such features and the framework architecture are described thoroughly in the [attached] ESP-IDF Mesh Stack Practical Guide.

<p align="center">
 <img src="https://bgrfcw.db.files.1drv.com/y4myCjZw3igFHv1IDcmT5-sQyeMS9P1PiP7m-4wYmMuqsqqz5wv-prKJGlvd6LCv3DO1RWBRXGxtMT0BmWw0LMtyVbusAWzWcBfq41vf5QAbTTGqX25LafvqCii5_9hESOTDweAEb56-x-i7UkKsRrA0v9MjHFiyPlW9jqf9ZzlYB0znBn_95F0B4u_u6Z4lt5Zh1FZODQF55zvWBN4Z9jJ3A?width=1346&height=2075&cropmode=none" width="75%" height="75%">
 </p>

The features offered by the application framework include:
 
* The possibility of customizing via the 'menuconfig' utility all aspects of mesh networking on the nodes, from the Mesh Network ID and the external router configuration to the organization mode used in the network (Self-Organized, Fixed-Root or Manual Networking), to configuring parameters relative to the network topology and root election, the possibility of addig node into mesh groups, and much more.

* A [comprehensive] code documentation and runtime logging of the evolution of the application's execution

* The following driver components provided as examples:

  - A Logging Driver, which performs a periodical logging of the main settings relative to mesh networking on a node, with the possibility of also logging the node's routing table and status of its Station and SoftAP interfaces.
  - A Sender Driver, which allows a node to send mesh packets with custom payload and data descriptor towards other nodes in the mesh network
  - A Receiver Driver, which allows a node to receive mesh packets destined to self, with the added possibility of replying to such packets with a predefined response
  - A SenderDS Driver, which allows a node to send data destined to an host external to the mesh network
  - A ReceiverDS Driver, which executed on the root node of the network allows it to receive the data to be forwarded towards the external router (where note that the IP sockets creation and use required to actually forward the data is not included in the application)
  - A Waive Driver, which executed on the root node in a Self-Organized mesh network allows it to waive its root status, thus triggering a new root election in the network, should its RSSI with the router fall below a predefined threshold or automatically after a set time interval
  
* The possibility of easily adding other driver components by providing them a flag in the Mesh Event Group and starting their tasks in the appropriate driver components starting functions (See pag. 58 of the guide and the meshbasics_driver.c file for an example).

Due to the [continuing] of my studies currently I have no plans on updating this framework or the related guide, even if feedback and comments are most appreciated.
