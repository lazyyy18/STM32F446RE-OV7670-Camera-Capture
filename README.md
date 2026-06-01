# STM32F446RE-OV7670-Camera-Capture

This project implements a simple embedded image capture system using the STM32 NUCLEO-F446RE development board and the OV7670 camera module. The OV7670 registers are configured through a software-based SCCB interface implemented with GPIO bit-banging. After initialization, the camera outputs image data, which is received by the STM32 and transmitted to the PC through UART for image display.

## Project Overview

The main purpose of this project is to understand how an image sensor works with a microcontroller and how raw image data can be captured, transmitted, and displayed.

This project focuses on:

* OV7670 camera initialization
* Software SCCB communication
* OV7670 register configuration
* RGB565 image data capture
* UART image data transmission
* PC-side image display

## Hardware

* STM32 NUCLEO-F446RE development board
* OV7670 camera module
* USB cable for programming and UART communication
* Jumper wires

## Features

* Configure OV7670 registers using software SCCB
* Initialize the OV7670 camera module
* Capture image data from the OV7670
* Handle RGB565 image format
* Transmit image data from STM32 to PC through UART
* Display the captured image on the PC side

## Technical Details

In this project, the SCCB interface is implemented in software using GPIO pins instead of using the STM32 hardware I2C peripheral. This method manually controls the SCCB clock and data signals to configure the internal registers of the OV7670 camera module.

After the camera is initialized, the OV7670 outputs image data to the STM32. The STM32 receives the image data, organizes it according to the selected image format, and sends the data to the PC through UART. A PC-side program can then receive the transmitted frame data and display the captured image.

## System Flow

1. Initialize STM32 peripherals
2. Configure OV7670 registers through software SCCB
3. Set the OV7670 output format
4. Capture image data from the OV7670
5. Transmit image data to the PC through UART
6. Display the captured image on the PC side

#Example
<img width="160" height="120" alt="ov7670_frame_rgb565_normal" src="https://github.com/user-attachments/assets/e4b6805a-c592-4664-a401-60658520669b" />


## What I Learned

Through this project, I learned how to configure an external camera module, implement SCCB communication using GPIO bit-banging, receive image data from an image sensor, handle RGB565 image format, and transmit image frames to a computer through UART.

This project also helped me gain a better understanding of the integration between embedded systems and image processing.

