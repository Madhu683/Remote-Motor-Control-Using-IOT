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

