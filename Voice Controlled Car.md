# Voice Controlled Car

This is the link for the project: [https://www.hackster.io/aqarrout/voice-controlled-car-ee1464]

**Project Description** : This bot works on Voice Recognition Technology. 

The circuit includes Arduino UNO Board, HC-05/HC-06 Bluetooth Module, L293D Motor Driver IC, a pair of DC Geared Motors of 200 RPM and a 9V Battery.

The voice Commands are processed by phone, and speech-to-text conversion is done within the app using Google’s speech-recognition technology. Text is then sent to the receiver side via Bluetooth. Text received via Bluetooth is forwarded to Arduino Uno board, Arduino controls the movements of the robot accordingly in forward, backward, Turning Right, Turning Left & Stop if the text is a matching string. Here, the transmitter is a Android smartphone with application connected to a bluetooth transceiver, on the reciever side is this bluetooth HC-05 connected to Arduino Uno board which is further connected to L293D Motor Driver controlling Left motor and right motor.

**Problem Statement** : To design a Car (Bot) that can be controlled by voice commands like 'RIGHT', 'LEFT', 'FORWARD', 'BACKWARD', 'STOP'.

**Ideation**: Understanding the Car's Mechanism:

* **Smartphone App** => **Bluetooth Transceiver** => **Microcontroller (Arduino)** => **Motor Driver & Motors**
* Part of the pipeline to break: 

| **Part of the Pipeline** | **Feasibility** | **Advantages** | **Disadvantages** |
|---|---|---|--|
| Smartphone App | Hard to code an app. | Easily available for many PANs | Security issues; can be hacked easily |
| Bluetooth Transceiver | Easy to use SPP; widely used also | Low power consumption. Better range than IR. Cheap in terms of cost. | Low bandwidth compared to WIFI. Short range communication. | 
| Arduino/ Microcontroller | Usually hard, unless very skilled and experienced | Easily programmable, as it has many libraries to work with. | Limited executions. Hard for beginners.|
| Motor Driver & Motors | Easy to control. They can be easily customised! | Works in smaller scales of Voltage and current. Variety of options available. | H-bridge ICs come in different datasheets, making it a little difficult task. Cost is fine. |

* Choosing a Pipeline: 

From the Above, we can choose Bluetooth Transciever or Motor driver & Motors for improvements. Here, they have chosen HC05/HC06 Bluetooth tranceiver; The difference is just master-slave operations, with upto 10m sensitivity circle.

Motor drivers, these listen to low voltage powered Arduino and controls an actual motor which needs high input voltage. L293d/ L298n can be the options. L293 is better as its supply cuurent is 600mA and o/p voltage upto 36V, with quadruple half bridge can drive 4 motors easily for this sort of application.

**Prototyping phase:** Here, we choose the right components, build, code, test and debug!

