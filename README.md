<br/> <div align="center"> <img src="img/logo.png"> </div> <br/> <div align="center">
Arduino library for using Qorvo's DW1000
 IC and related modules




</div>
Differences from F-Army/arduino-dw1000-ng

This project is a fork of F-Army/arduino-dw1000-ng
.

I've developed a Fast RTLS system using 4 anchors, including:

NLOS/LOS detection algorithm

Retry logic

Several filtering methods for RTLS

Added small delays to improve stability on the DWM1000 SPI bus

Features

RTLS with 4 anchors
(You can apply weighting techniques or even discard unreliable TWR range results if desired.)
<img width="333" height="288" alt="image" src="https://github.com/user-attachments/assets/81c03e5f-2268-4526-b052-9a2e5adf3d90" />

Retry Logic
(This is the biggest difference from the original arduino-dw1000-ng.
I modified the retry logic, which significantly increased RTLS speed!)
<img width="733" height="447" alt="image" src="https://github.com/user-attachments/assets/0340e495-c9c9-4a98-8bec-5a8d768adfe8" />

Reduced delay
(You can achieve higher speed by reducing delays or tuning RTLS parameters in this library.)

NLOS/LOS Detection
(Includes a detection logic based on signal quality registers in the DWM1000 — for example, FP Power, Rx Power, FP Ampl, and SNR.)
<img width="1025" height="356" alt="image" src="https://github.com/user-attachments/assets/cccea283-ef4c-491f-9df9-24ec7a7357f6" />

Filtering Logic
(Includes custom filtering functions for more stable position estimation.)

<br/>
Supported Devices








Specific tested devices with pinout information are listed in the Wiki
.

Installation

Requires C++11 support (Arduino IDE >= 1.6.6 supports C++11)

Download the ZIP file of the master branch or the latest release and save it locally.

Open the Arduino IDE and go to Sketch → Include Library → Add .ZIP Library...

Select the downloaded ZIP file of this DW1000 library.

You should now see the library in the list and be able to access examples in the IDE.

Usage

Check the examples folder for basic usage.

The Decawave documentation
 is also very helpful if you want to understand this project in depth.

Contributors
<ul> <li><b>Jaeyun 'jjletsgo' Jung</b>: https://github.com/jjletsgo</li> </ul>
License

This project is licensed under the MIT License (see LICENSE.md
).
Some files are dual-licensed under Apache 2.0/MIT, since this project is a fork of thotro/arduino-dw1000
.
