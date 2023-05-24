MouseJack-RF-Nano ![projects-microcontroller](https://img.shields.io/badge/projects-microcontroller-blue)
-----------------

MouseJack-RF-Nano is a project, based on **uC_mousejeck** by **[insecuritythings](https://github.com/insecurityofthings/uC_mousejack)**, to get [Mousejack](https://www.mousejack.com) attacks into a small embedded device, with the form factor of a key chain.

Building the device is straight-forward, and the code provides a tool to use Duckyscript to launch automated keystroke injection attacks against Microsoft and Logitech devices.

Construction
------------

Components list:
 - [RF-Nano](https://www.ebay.com.au/itm/134057587798?hash=item1f36747456:g:Dq4AAOSwW5diNG2K).

  ![RF-Nano](https://raw.githubusercontent.com/davidmgilbert/MouseJack-RF-Nano/master/img/rf-nano.jpeg)



 Compiling & Upload
 --------

 To build the software, download and install the [PlatformIO IDE](http://platformio.org/platformio-ide).

 Before building the software, be sure to modify the `attack.h` file using the `attack_generator.py` script:

 ```
MouseJack-RF-Nano $ cd tools
 tools $ ./attack_generator.py ducky.txt
 ```

 In the example above, the ducky.txt file contains our [Duckyscript](https://docs.hak5.org/hak5-usb-rubber-ducky/duckyscript-tm-quick-reference). The `attack_generator.py` script will "compile" the ducky script into the `attack.h` file, which is included in `main.cpp`. This simplifies the code and makes it more compact.

 Testing
 -------

 Once you power the device on, the internal LED connected to pin 13 (called ledpin in the code), will blink two times for each pass over the entire channel range. When it sends an attack, the LED will glow solid.

 If you monitor the serial port using the PlatformIO IDE, you will see the radio information details and a lot of debugging information being printed while scanning and during attack.

 Warning: No interaction is required to initiate an attack.

 Future
 ------

 As future work:
 - to create a python program to interact with arduino, passing parameters to the runtime attack;
  
