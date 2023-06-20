# ISMIN_Prototype_Project_-_Air_Guitar
This project is the development of a prototype of an Air Guitar. This project was developed during the prototyping discipline of the microelectronics and informatics course at the École des Mines de Saint-Etienne - ISMIN.

The STM32F301K8T6 microcontroller was used to capture the frequency coming from the conditioning circuit to output a PWM frequency which corresponds to a musical note based on buttons pressed in order to simulate a guitar.

In this project, Timers 1 and 2 were configured for reading and generating frequencies, UART for serial communication, and GPIO pin configuration.

The code contains the following functions:
* HAL_TIM_IC_CaptureCallback to capture the frequency of an external circuit which contains a metal plate
* Check_Frequency to indicate if the captured frequency is below a certain frequency (in this project: 42kHz) which indicates if the hand, or some body, is close to the metal plate or not
* Check_Pin to detect which buttons are pressed
* Config_PWM to produce a PWM output frequency from the keys pressed in Check_Pin
