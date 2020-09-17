# Task Scheduler
### Cooperative multitasking for Arduino, ESPx, STM32 and other microcontrollers
#### Version 3.2.0: 2020-08-16 [Latest updates](https://github.com/arkhipenko/TaskScheduler/wiki/Latest-Updates)

[![arduino-library-badge](https://www.ardu-badge.com/badge/TaskScheduler.svg?)](https://www.ardu-badge.com/TaskScheduler)[![xscode](https://img.shields.io/badge/Available%20on-xs%3Acode-blue?style=?style=plastic&logo=appveyor&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAAZQTFRF////////VXz1bAAAAAJ0Uk5T/wDltzBKAAAAlUlEQVR42uzXSwqAMAwE0Mn9L+3Ggtgkk35QwcnSJo9S+yGwM9DCooCbgn4YrJ4CIPUcQF7/XSBbx2TEz4sAZ2q1RAECBAiYBlCtvwN+KiYAlG7UDGj59MViT9hOwEqAhYCtAsUZvL6I6W8c2wcbd+LIWSCHSTeSAAECngN4xxIDSK9f4B9t377Wd7H5Nt7/Xz8eAgwAvesLRjYYPuUAAAAASUVORK5CYII=)](https://xscode.com/arkhipenko/TaskScheduler)

### OVERVIEW:
A lightweight implementation of cooperative multitasking (task scheduling) supporting:
1. Periodic task execution, with dynamic execution period in `milliseconds` (default) or `microseconds` (if explicitly enabled) – frequency of execution
2. Number of iterations (limited or infinite number of iterations)
3. Execution of tasks in predefined sequence
4. Dynamic change of task execution parameters (frequency, number of iterations, callback methods)
5. Power saving via entering **IDLE** sleep mode when tasks are not scheduled to run
6. Support for event-driven task invocation via Status Request object
7. Support for task IDs and Control Points for error handling and watchdog timer
8. Support for Local Task Storage pointer (allowing use of same callback code for multiple tasks)
9. Support for layered task prioritization
10. Support for `std::functions` (tested on `ESPx` only)
11. Overall task timeout
12. Static and dynamic callback method binding
13. CPU load / idle statistics for time critical applications
14. Scheduling options with priotity for original schedule (with and without catchup) and interval

Scheduling overhead: between `15` and `18` microseconds per scheduling pass (Arduino UNO rev 3 @ `16MHz` clock, single scheduler w/o prioritization)

**TaskScheduler** was tested on the following platforms:
* Arduino Uno R3
* Arduino Nano
* Arduino Micro
* ATtiny85
* ESP8266 (Node MCU v2.0)
* ESP32
* Teensy (tested on Teensy 3.5)
* STM32F1 (tested on Mini USB STM32F103RCBT6 ARM Cortex-M3 leaflabs Leaf maple mini module F)
* MSP430 and MSP432 boards
---
![TaskScheduler process diagram](https://github.com/arkhipenko/TaskScheduler/raw/master/extras/TaskScheduler_html.png)
---
### Changelog is located [here.](https://github.com/arkhipenko/TaskScheduler/wiki/Changelog)


#### For detailed functionality overview please refer to TaskScheduler documentation in the 'extras' folder or in the [Wiki page](https://github.com/arkhipenko/TaskScheduler/wiki).

### Check out what TaskScheduler can do:

* [3 Devo](http://3devo.eu/) - Quality 3D printing filament, now made accessible and affordable
(http://3devo.eu/license-information/)


* [Houston midi](https://github.com/chaffneue/houston) clock project - TaskScheduler with microseconds resolution
    >by chaffneue:
    >>My first arduino project. It's a multi-master midi controller with a shared clock and
     auto count in behaviour.

	 youtube: https://www.youtube.com/watch?v=QRof550TtXo


* [Hackabot Nano](http://hackarobot.com/) by Funnyvale -  Compact Plug and Play Arduino compatible robotic kit
     https://www.kickstarter.com/projects/hackarobot/hackabot-nano-compact-plug-and-play-arduino-robot


* Arduino Nano based Hexbug Scarab Robotic Spider
    (by arkhipenko: http://www.instructables.com/id/Arduino-Nano-based-Hexbug-Scarab-Robotic-Spider/)

* Wave your hand to control OWI Robotic Arm... no strings attached
    (by arkhipenko: http://www.instructables.com/id/Wave-your-hand-to-control-OWI-Robotic-Arm-no-strin/)


* APIS - Automated Plant Irrigation System
    (by arkhipenko: http://www.instructables.com/id/APIS-Automated-Plant-Irrigation-System/)


* IoT APIS v2 - Autonomous IoT-enabled Automated Plant Irrigation System
    (by arkhipenko: http://www.instructables.com/id/IoT-APIS-V2-Autonomous-IoT-enabled-Automated-Plant/)

* Interactive Halloween Pumpkin
    (by arkhipenko: http://www.instructables.com/id/Interactive-Halloween-Pumpkin/)

* Interactive Predator Costume with Real-Time Head Tracking Plasma Cannon
    (by arkhipenko: https://www.instructables.com/id/Interactive-Predator-Costume-With-Head-Tracking-Pl/)

* Party Lights LEDs music visualization
    (by arkhipenko: https://www.instructables.com/id/Portable-Party-Lights/)
    
