# The Ultimate Binary Watch

This is the link for the project: [https://www.instructables.com/id/The-Ultimate-Binary-Watch/]

**Project Description** : 
The components include LEDs, Microcontroller (Atmega328P-AU), RTC (Real-Time Clock) because of its accuracy, DC-DC Boost Converter
IC, LiPo battery.

A binary watch is a clock that displays time in binary format, specifically BCD (Binary Coded Decimal).
This binary watch has many features such as Binary RGB interface ,Date display , Stopwatch, Alarm, Long battery life, USB charging
and an easily customisable software for the user.

The binary format goes like; there is a 4X4 grid with h h : m m on one edge and 1 2 4 8 on the other, therefore all digits from
0-9 can be represented on the watch by lighting up the LEDs of the respective blocks and weights will add up to give the number.

**Problem Statement** : The idea is to create a multifunctional binary watch; displaying time, date, stopwatch and alarm.
Major constraints are Long battery life and Size of the wrist watch!

**Ideation**: Understanding the Watch's Mechanism:

* **Charging IC & Battery** => **DC-DC Boost Converter** => **Microcontroller** => **RTC (Real Time Clock)** => **LED Array**
* Part of the pipeline to break: 

| **Part of the Pipeline** | **Feasibility** | **Advantages** | **Disadvantages** |
|---|---|---|--|
| Charging IC & Battery | Energy providers for the circuit | Many options of this are available (We can choose subject to the size constraints) | Power required and available size of batteries mismastch, Charging IC needs to be compatible with the battery opted|
|DC-DC Boost Converter | Can be figured by  looking at the circuit for voltage and current constraints | Capable to step up the voltage of lowest component count possible.  Input current is continuous which is very desirable  | Usually expensive and difficult to control.| 
| Microcontroller| Usually hard, unless very skilled and experienced | Easily programmable, as it has many libraries to work with. | Limited executions and Hard for beginners.|
| RTC (Real Time Clock) | Much needed, used for real time data collection | Low power consumption, High accuracies available | Manual Recalibaration (As there is no internet connection), It is more tedious than batch-processing of data |
|LED Array| Very much feasible | Cheap, customisable, RGB colours available | Voltage precautions, delicate life-span |


* Choosing a Pipeline: 

From the Above, we can choose Charging ICs, RTC and LED arrays for modification. The battery needed to be small enough so that 
it could fit inside the watch enclosure without making it look bulky, 250mA LiPo batteries and compatible charging IC (limiting 
the rate at which electric current is added to or drawn from electric batteries) were used.

For RTC, since there is no internet connectivity the user would need to recalibrate it manually. M41T62 RTC with high accuracy, 
I2C compatibility and the ulta low current consumption was used.

LED arrays should be very small (2mm X 2mm), they come in various colours and are highly inexpensive.

**Prototyping phase:** Here, we choose the right components, build, code, test and debug!
