# Remote-Motor-Control-Using-IOT
The project aims to provide the user with the facility of turning on/off a motor that is remotely
located from his mobile app. The app will have buttons to turn the motor on and off. The
specific button press event triggered will be used to send a motor command to the Firebase
database in the cloud. This motor command will be read by the GISMO-V board which has an
ESP32 microcontroller and can be connected to the Internet and fetch the motor command from
the cloud database. Based on the command the ESP32 will operate a relay to appropriately
switch the motor. The ESP32 controller is a 32-bit dual core processor with Wi-Fi and
Bluetooth capabilities built on-chip. The Wi-Fi capability is used to join a Wi-Fi network and
connect to the Internet. The motor commands are pushed to a cloud database – Google’s
Firebase which is created for the project.. The command is read by the ESP32 and used to
switch the motor on or off. The database credentials – the host URL and the database
authentication key are to be fed into the firmware. The Firebase database is a key-value based
database and using the Firebase credentials and the key the commands are accessed .

The different components in the project are:
![blockDiagram](https://user-images.githubusercontent.com/70106840/131373097-47819f9a-40a4-4b1f-9bfd-a5bf5142a873.png)

Hardware
--------

The hardware for the project consists of:
- GISMO-V board with:
o ESP32 dual-core 32-bit processor with Wi-Fi and BLE
o Relay for switching the motor
o 0.96” OLED display with 128x64 resolution
The relay used is a sugar cube relay which operates at 5V. A transistor drive circuit is present
on the board for driving the relay. The base of the transistor is connected to GPIO13. By making
this GPIO pin high/low the relay can be switched on/off. The Normally Open(NO) contacts of
the relay are brought out onto terminal blocks. An AC operated contactor is switched on/off
using the relay and the contactor contacts are used to switch on/off the motor.
The OLED display is a graphic display with I2C interface to the microcontroller. The SCL
and SDA lines of the OLED display are connected to GPIO22 and GPIO21 pins of the
ESP32. These are the I2C pins of the ESP32. The supply voltage for the OLED display is
3.3V
The ESP32 development board used is the ESP32 Dev Kit. The ESP32 board has a micro
USB for programming, powering up and for transfer of data on serialline to and from the
laptop. It has an on-board LED connected to GPIO2 which can be used for debugging
purposes. It has a RESET and a BOOT button. The BOOT button needs to be kept pressed
while downloading the program to the board. The Dev Kit also has 4 MB of external flash
memory

