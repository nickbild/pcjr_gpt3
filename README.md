# IBM PCjr GPT-3

Ask the world's smartest IBM PCjr anything and it will answer using the GPT-3 deep learning language model.

![](https://raw.githubusercontent.com/nickbild/pcjr_gpt3/main/media/computer_angle_sm.jpg)

## How It Works

An IBM PCjr (MS-DOS 5.0, 640 KB RAM) has it's serial port connected to an RS-232 to USB adapter.  Since the serial port uses a non-standard 2x8 pin Berg connector (everything on a PCjr is non-standard), I hacked together an adapter that connects it to a standard DB-25 cable.  IBM did sell adapters like this, but I don't have one.  The PCjr is running the communications software package Kermit version 3.14.

The USB cable is connected to a Raspberry Pi 4.  A Python script runs on the Pi ([code here](https://github.com/nickbild/pcjr_gpt3/blob/main/pcjr_gpt3.py)) that accepts input coming in over the serial interface (from the user typing in Kermit the PCjr), and sends it to a GPT-3 language model accessible via the OpenAI API.  The API response is sent over serial back to the PCjr where it is displayed on the screen.  This creates an interactive question and answer interface running on the PCjr that leverages a deep learning language model on the backend.

## Media

The PCjr connected to a Raspberry Pi 4 via RS-232 serial:

![](https://raw.githubusercontent.com/nickbild/pcjr_gpt3/main/media/pcjr_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/pcjr_gpt3/main/media/monitor_front_sm.jpg)

A hacked together serial cable adapter:

![](https://raw.githubusercontent.com/nickbild/pcjr_gpt3/main/media/serial_cable_sm.jpg)

![](https://raw.githubusercontent.com/nickbild/pcjr_gpt3/main/media/serial_cable_close_sm.jpg)

## Bill of Materials

- 1 x IBM PCjr
- 1 x Raspberry Pi 4
- 1 x IBM PCjr serial cable adapter
- 1 x USB to Serial RS-232 Adapter

## About the Author

[Nick A. Bild, MS](https://nickbild79.firebaseapp.com/#!/)
