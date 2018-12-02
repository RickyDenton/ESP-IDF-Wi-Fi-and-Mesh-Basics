# ESP-IDF Mesh Stack Application Framework & Practical Guide

The purpose of this program is to provide a comprehensive framework for developing applications using the mesh networking functionalities currently offered by the ESP-IDF mesh stack as of version 3.1, which are described in detail along with the framework architecture in the attached *ESP-IDF Mesh Stack Practical Guide*.

<p align="center">
 <img src="https://bgrfcw.db.files.1drv.com/y4myCjZw3igFHv1IDcmT5-sQyeMS9P1PiP7m-4wYmMuqsqqz5wv-prKJGlvd6LCv3DO1RWBRXGxtMT0BmWw0LMtyVbusAWzWcBfq41vf5QAbTTGqX25LafvqCii5_9hESOTDweAEb56-x-i7UkKsRrA0v9MjHFiyPlW9jqf9ZzlYB0znBn_95F0B4u_u6Z4lt5Zh1FZODQF55zvWBN4Z9jJ3A?width=1346&height=2075&cropmode=none" width="75%" height="75%">
 </p>

The features offered by the application framework include:

* The possibility of customizing via the 'menuconfig' utility all aspects of mesh networking on nodes, from the Mesh Network ID and the external router configuration to the organization mode used in the network (Self-Organized, Fixed-Root or Manual Networking), from configuring network topology and root election parameters to the possibility of adding nodes to mesh groups, and much more.

* A detailed code documentation and runtime logging of the evolution of the application's execution.

* The following driver components provided as examples:

  - A *Logging Driver*, which performs periodic logging of the main settings relative to mesh networking on a node, with the added possibility of logging the node's routing table and the status of its Station and SoftAP interfaces.
  
  - A *Sender Driver*, which allows a node to send mesh packets with a custom payload and data descriptor to other nodes in the mesh network.
  
  - A *Receiver Driver*, which allows a node to receive mesh packets destined for itself, with the added possibility of replying to the sender with a predefined response.
  
  - A *SenderDS Driver*, which allows a node to send data destined for a host external to the mesh network.

  - A *ReceiverDS Driver*, which when executed on the root node allows it to receive the data to be forwarded to the external router (where note that the IP sockets creation and use required to actually forward the data is not included in the application).
  
  - A *Waive Driver*, which when executed on the root node in a Self-Organized mesh network allows it to waive its root status, thus triggering a new root election in the network, should its RSSI with the router fall below a predefined threshold or automatically after a set time interval.
  
* The possibility of easily adding other driver components by providing them with a flag in the Mesh Event Group and by creating their tasks in the appropriate driver components starting functions (see page 58 of the guide and the *meshbasics_driver.c* file for an example).

Due to the continuation of my studies, I currently have no plans to maintain or update this framework or the related guide, even if feedbacks and comments are most appreciated.
