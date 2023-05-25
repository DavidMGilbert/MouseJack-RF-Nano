![MouseJack-RF-Nano](https://socialify.git.ci/DavidMGilbert/MouseJack-RF-Nano/image?description=0&font=Raleway&forks=1&issues=1&language=1&owner=1&pattern=Circuit%20Board&pulls=1&stargazers=1&theme=Dark)


<h2 align=center>
  <a href="#">
    <img src="https://forthebadge.com/images/badges/built-by-codebabes.svg">
  </a>
  <a href="#">
    <img src="https://forthebadge.com/images/badges/powered-by-coffee.svg">
  </a>
  <a href="#">
    <img src="https://forthebadge.com/images/badges/pretty-risque.svg">
  </a>
  <a href="#">
    <img src="https://forthebadge.com/images/badges/made-with-out-pants.svg">
  </a>
 </h2>

<h2 align=center> ⚠ PLEASE NOTE: This code is only for educational purposes. ⚠ </h2>
<h2 align=center> ⚠ If you do something illegal expect to be held responsible for your own actions. ⚠ </h2>

<h2 align=center> 📑 Introduction </h2>

MouseJack-RF-Nano is a project, based on **uC_mousejeck** by **[insecuritythings](https://github.com/insecurityofthings/uC_mousejack)**, to get [Mousejack](https://www.mousejack.com) attacks into a small embedded device, with the form factor of a key chain.

Building the device is straight-forward, and the code provides a tool to use Duckyscript to launch automated keystroke injection attacks against Microsoft and Logitech devices.

<h2 align=center> 🛒 Shopping List</h2>
<center><img height=200 width=auto src="https://raw.githubusercontent.com/davidmgilbert/MouseJack-RF-Nano/master/img/rf-nano.jpeg"></center>
<h2 align=center>
  <a href="https://www.davidmgilbert.com/product/mousejack-rf-nano/">
    <img src="https://forthebadge.com/images/badges/check-it-out.svg">
  </a>

<h2 align=center> 👨🏻‍💻 How to get started? </h2> 

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

  ⚠ ***Warning: No interaction is required to initiate an attack.*** ⚠ 

<h2 align=center> 📝 How to Contribute? </h2>  

- Take a look at the Existing Issues or create your own Issues!
- Wait for the Issue to be assigned to you after which you can start working on it.
- Fork the Repo and create a Branch for any Issue that you are working upon.
- Create a Pull Request which will be promptly reviewed and suggestions would be added to improve it.
- Share your wins and your fails when trying this out!

<h2 align=center> ✨ Contributors ✨ </h2>
  
  <table>
	<tr>
		<td>
			<a href="https://github.com/DavidMGilbert/MouseJack-RF-Nano/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=DavidMGilbert/MouseJack-RF-Nano" />
      </a>
		</td>
	</tr>
</table>

Contributions of any kind welcome!

<h1 align=center> Project Admin </h1>
<p align="center">
  <a href="https://www.davidmgilbert.com"><img src="https://avatars.githubusercontent.com/u/118702908?v=4" width=150px height=150px /></a>   

<h1 align=center>Happy Hacking 👨‍💻</h1>
