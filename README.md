[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot)
![Project](https://img.shields.io/badge/Project-STM32-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# STM32-based-Bluetooth-Radio-Control-Car-Robot
<strong>Solo Project: STM32-based BTRC Car Robot</strong><br><br>
In operation, this robot car requires a battery as its power supply. Then the user can control its movement by using a bluetooth signal. If the receiver is close to the transmitter, the signal generated will be stronger, while on the contrary, the signal generated will be weaker. This project prioritizes UART: Hardware Serial as a means of communication.

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | STM32F103C8T6 |
| Code Editor | Arduino IDE |
| Programmer Tools | FTDI FT232RL |
| Driver | USB-Serial CDM |
| Communications Protocol | Universal Asynchronous Receiver-Transmitter (UART) |
| Application Support | • STM32CubeProgrammer<br>• Bluetooth RC Controller |
| Programming Language | C/C++ |
| Actuators | Gear Motor / Motor DC (x2) |
| Sensor | JDY-31 SPP-C: Bluetooth Module (x1) |
| Other Components | • Mini USB cable - USB type A (x1)<br>• Micro USB cable - 2 pin JST (x1)<br>• Jumper cable (1 set)<br>• KCD11: Rocker Switch SPST (x1)<br>• Li-ion battery 18650 (x2)<br>• 2-Slot series battery holder (x1)<br>• Robot wheels (x2)<br>• Caster wheel (x1)<br>• Motor driver L298N (x1)<br>• Car robot frame (x1)<br>• Spicer bolts (1 set)<br>• Bolts plus (1 set)<br>• Nuts (1 set) |

<br><br>

## Download & Install
1. Arduino IDE

   <table><tr><td width="810">
         
   ```
   https://www.arduino.cc/en/software
   ```

   </td></tr></table><br>

2. USB-Serial CDM

   <table><tr><td width="810">

   ```
   https://bit.ly/CDM_Driver
   ```

   </td></tr></table><br>

3. STM32CubeProgrammer

   <table><tr><td width="810">
   
   ```
   https://bit.ly/STM32_Cube_Programmer
   ```

   </td></tr></table>
   
<br><br>

## Project Designs
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Pictorial Diagram</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/85978010-4eb6-4a6b-ad12-c6c0dd551e97" alt="Block-Diagram"></td>
<td><img src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/60a8106e-751d-4c63-96d3-61c612d889b4" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Wiring</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/3636a8db-2c91-4955-bb08-6b7eb2b5b114" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Basic Knowledge
Basically, a device can be communicated with other devices either wirelessly or by cable. Communication between commonly used hardware is ``` Serial Communication ```. It can be known that there are three types of ``` Serial Communication ```, which include: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, and ``` I2C (Inter Integrated Circuit) ```. There are two kinds of ``` UART Serial Communication ```, namely ``` Hardware Serial ``` and ``` Software Serial ```. ``` Hardware serial communication ``` can be done by connecting the ``` TX ``` and ``` RX ``` pins ``` crosswise ``` on each development board, for example: ``` RX-TX ```, then ``` TX-RX ```. The ``` TX ``` pin is for ``` sending data ```, while the ``` RX ``` pin is for ``` receiving data ```.

<br><br>

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open this project by clicking ``` File ``` -> ``` Open ``` :

   <table><tr><td width="810">
      
      ``` stm32_btrc_car_robot.ino ```

   </td></tr></table><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link :
      
      ```
      https://github.com/stm32duino/BoardManagerFiles/raw/main/package_stmicroelectronics_index.json
      ```

   </td></tr></table><br>
   
3. ``` Board Setup ``` in Arduino IDE

   <table>
      <tr><th width="810">

      How to setup the ``` STM32F103C8T6 ``` board
            
      </th></tr>
      <tr><td>
         
      • Click ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` STM32 MCU based boards ```.

      • Then click ``` Tools ``` -> ``` Board ``` -> ``` STM32 boards groups ``` -> ``` Generic STM32F1 series ```.

      </td></tr>
   </table><br>
   
4. ``` Change Board Part Number ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Tools ``` -> ``` Board part number ``` -> ``` BluePill F103C8 ```

   </td></tr></table><br>
   
5. ``` Change U(S)ART Support ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Tools ``` -> ``` U(S)ART Support ``` -> ``` Enabled (generic 'Serial') ```

   </td></tr></table><br>

6. ``` Change Upload Method ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Tools ``` -> ``` Upload method ``` -> ``` STM32CubeProgrammer (Serial) ```

   </td></tr></table><br>
   
7. ``` Port Setup ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Port ``` -> Choose according to your device port ``` (you can see in device manager) ```

   </td></tr></table><br>

8. Before uploading the program please click: ``` Verify ```.<br><br>

9. If there is no error in the program code, then please click: ``` Upload ```.<br><br>

10. If there is still a problem when uploading the program, then try checking the ``` driver ``` / ``` port ``` / ``` others ``` section.

<br><br>

## Programmer Tools Setup: FTDI FT232RL
1. ``` Programming Mode ``` :
      
   • Make sure you haven't uploaded the program.
   
   • Make sure the ``` BOOT0 jumper ``` position on the ``` STM32F1 ``` is at position ``` 1 ```.
   
   • Make sure the ``` BOOT1 jumper ``` position on the ``` STM32F1 ``` is at position ``` 0 ```.
   
   • Make sure the ``` Vout jumper ``` position on the ``` FTDI ``` is at position ``` 3.3V ```.

   • Connect this ``` STM32F103C8T6 board ``` to ``` FTDI ```.
      
      <img width="810" src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/3673fac7-49e1-43e7-8c7a-1bfaf060d7cb" alt="programming-mode">

   • Then connect the ``` FTDI ``` to your ``` PC/Laptop ``` with a ``` Mini USB - USB type A ``` cable.

   • Press the ``` Reset ``` button so that all programs embedded in this ``` STM32 board ``` become clean (ready to be reprogrammed).
   
   • Compile and upload your program through a code editor, in this case the ``` Arduino IDE ```.<br><br><br>
   
2. ``` Operating Mode ``` :
   
   • Make sure to upload the program.

   • Remove the ``` FTDI ``` from the device.
   
   • Make sure the ``` BOOT0 & BOOT1 jumper ``` position on the ``` STM32F1 ``` is at position ``` 0 ```.
      
      <img width="810" src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/25e28727-b9bf-4218-9919-a5c807b8cb44" alt="operating-mode">
   
   • The program code that has been embedded in this ``` STM32 board ``` is ready for operation (no more programming activities).

   • To power up this ``` STM32F1 board ```, you can use an external power supply such as a battery or something else.<br><br><br>

<strong>Notes :</strong>

<table><tr><td width="840">
   
   • To upload the program, besides using the ``` FTDI FT232RL ```, you can also use other programming tools such as: ``` ST-Link/V2 ``` or ``` PL2303 ```.

   • Based on experience, I admit that using the ``` ST-Link/V2 ``` is much better than the ``` USB PL2303 ``` as well as ``` FTDI FT232RL ``` because the program upload can be done automatically without the need to move the pin socket for booting purposes.

</td></tr></table>

<br><br>

## Bluetooth RC Controller Setup
1. Go to ``` Assets/APK ``` directory to get the app called ``` Bluetooth RC Controller ``` -> then install the app on your gadget.
   
2. Open ``` Bluetooth RC Controller ``` app.
   
3. Turn on ``` bluetooth ```. 
   
4. Click ``` gear ``` button -> select ``` Connect to car ```.
   
5. Click ``` Scan for devices ``` button -> select ``` JDY-31-SPP ```.

6. Then ``` pairing device ``` by entering the password: ``` 0000 ``` or ``` 1234 ```.
  
7. The user interface is ready to use. This is as seen in the following image.

   <img width="810" src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/6ccfbbaa-a972-4437-a08d-2b40755badef" alt="user-interface">

<br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>

5. Please enjoy [Done].

<br><br>

## Highlights
<img width="840" src="https://github.com/devancakra/STM32-based-Bluetooth-Radio-Control-Car-Robot/assets/54527592/8cc918a3-6a37-4f63-ab0c-0a426ced48ab" alt="rc-car-robot">

<br><br>

## LICENSE
MIT License - Copyright © 2023 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
