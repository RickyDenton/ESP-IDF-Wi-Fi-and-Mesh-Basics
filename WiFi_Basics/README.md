# ESP-IDF Mesh Stack Application Framework & Practical Guide

The purpose of this program is to provide a comprehensive framework for developing applications using the Wi-Fi networking features currently offered by the ESP-IDF Wi-Fi stack as of version 3.1, where a comprehensive analysis of such features and the framework architecture are described thoroughly in the [attached] *ESP-IDF Wi-Fi Stack Practical Guide*.

<p align="center">
 <img src="https://q2nfcw.db.files.1drv.com/y4mx-hbtVtpp8io0Kd9QSXMKL1gpurNeiPsbOCYSccMA7PY0VMonmGKwe4CBRePF4BwiqSI8kVlA1546erWmk6sbYcvZd6rhHVUEaZ9hUD-5Z6NU9aeRqdrNHpUh-2ITVko5lt2zWSSBzvtrrMp---gpwd_IRTtj64-Lb3NJ2UaugICoaBS4O3O79CTwBBpzURVO67xJOVW3l99kTCSXeIqhw?width=1278&height=1725&cropmode=none" width="75%" height="75%">
 </p>

The features offered by the application framework include:
 
* The possibility of customizing via the 'menuconfig' utility most of the aspects of Wi-Fi networking on a device, from its Station and/or SoftAP base configurations, their MAC and IP addresses, the power saving mode to use on the Station interface, and more.

* A [comprehensive] code documentation and runtime logging of the evolution of the application's execution

* Three driver components provided as example which perform a periodical logging of the Station and SoftAP interfaces configurations
  
* The possibility of easily adding other driver components by providing them a flag in the Wi-Fi Event Group and starting their tasks in the appropriate driver components starting functions (See pag. 35 of the guide and the *wifibasics_driver.c* file for an example).

Due to the [continuing] of my studies currently I have no plans on updating this framework or the related guide, even if feedback and comments are most appreciated.
