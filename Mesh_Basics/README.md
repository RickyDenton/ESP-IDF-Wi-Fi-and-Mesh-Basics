# ESP-IDF Mesh Stack Practical Guide & Application Framework

The purpose of this program is to provide a framework for developing applications using the mesh networking functionalities currently offered by the ESP-IDF mesh stack as of version 3.1, where a comprehensive analysis of the features offered, the modular architecture, and the components constituting the application are described thoroughly in the ESP-IDF Mesh Stack Practical guide [attached].

<p align="center">
 <img src="https://bgrfcw.db.files.1drv.com/y4myCjZw3igFHv1IDcmT5-sQyeMS9P1PiP7m-4wYmMuqsqqz5wv-prKJGlvd6LCv3DO1RWBRXGxtMT0BmWw0LMtyVbusAWzWcBfq41vf5QAbTTGqX25LafvqCii5_9hESOTDweAEb56-x-i7UkKsRrA0v9MjHFiyPlW9jqf9ZzlYB0znBn_95F0B4u_u6Z4lt5Zh1FZODQF55zvWBN4Z9jJ3A?width=1346&height=2075&cropmode=none" width="75%" height="75%">
 </p>
 
Features offered by the framework include:

* The possibility of customizing via the 'menuconfig' utility all the parameters relative to the mesh network to develop, from the Mesh Network ID and external router configuration, to the type of organization used in the network (Self-Organized, Fixed-Root or Manual Networking), to network topology parameters, root election parameters, the possibility of adding nodes into mesh groups, and more
* A [comprehensive] logging of the application execution and the mesh events raised by the mesh stack
* The following driver components provided as example:
  - A Logging Driver, which performs a periodical logging of the state of the node in the mesh network, along with its routing table and possibly the status of its Station and SoftAP interfaces
  - A Sender Driver, which allows a node to send mesh packets with a custom payload and data descriptor to other nodes in the mesh network
  - A Receiver Driver, which allows a node to receive mesh packets destined to it and possibly "reply" to them
  - A SenderDS Driver, which allows a node to send data towards an external host outside the mesh network
  - A ReceiverDS Driver, which executed on the root node allows it to receive data to forward towards the external DS (where note that the creation and use of IP sockets to forward data to the external router is not provided)
  - A Waive Driver, which in a Self-Organized mesh network allows the root node to waive its root status should its RSSI with the router fall below a custom threshold or automatically after a set time interval
* The possibility of easily adding driver components by associating them a flag in the Mesh Event Group and by starting their tasks in the appropriate driver starting functions (see Pag. 58 of the guide and the meshbasics_driver.c file for a better explanation).

Due to the [continuing] of my studies I currently have no plans on updating the guide or the associated framework, even if feedback and comments are most appreciated 
