# HowTo-CreateNewSTM32Project

## Summary
This HowTo goes through setting up a new STM32 project from scratch via a simple example. The
example is with the NUCLEO-F401RE board and prepares a project to use PA5 (Port A Pin 5)
to control an LED on the board.

## Content
- Notes
- Download the STML32CubeIDE
- Download the STLink
- Setup PA5
- Generate Code
- Issues

## Notes
This document will use an example to go through setting up a project.

## Download the STML32CubeIDE

## Download the STLink

## Setup PA5
To setup PA5 (Port A - Pin 5), go to the projects .ioc file, click on PA5 within the 
STM32CubeMX perspective (this is where you see the content of the .ioc file). Then
set it to GPIO_Output (we use GPIO_Output, because it is an LED and we want output
from the MCU to control the LED, if we had a sensor we might use GPIO_Input so that
the MCU could receive input from the sensor).

## Generate Code
This will happen automatically when the .ioc is modified then saved.

## Issues
### Code Generate could not be done due to missing firmware
For this board if the code can not be automatically generated, go to **Help** ->
**Manage Embedded Software Packages**, then under **STM32CubeF4** install the 
latest version (requires you to be logged in). This resolved my code generation
issue.