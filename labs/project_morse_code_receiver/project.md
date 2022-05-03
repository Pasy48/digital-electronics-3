# MORSE CODE RECEIVER

### Team members

* Dominik Vaško 
* Jan Mucha 
* Martin Paseka 
* Gabriel Škápík

Link to your GitHub project folder:

   [PROJECT REPOSITORY](https://github.com/Hans22301/digital-electronics-1/tree/main/labs/project_morse_code_receiver)


### Table of contents
* [Project objectives](#objectives)
* [Hardware description](#hardware)
* [VHDL modules description and simulations](#modules)
* [TOP module description and simulations](#top)
* [Video](#video)
* [References](#references)


<a name="objectives"></a>
## Project objectives

As main objective of our project  we see learning how direct hardware programming works.

In this exact project  is our objective to complete "Morse code reciever" and we decided to  devide this into smaller objectives:
1. Create character map for seven segment display that will work for all  characters and numbers.

![your figure](https://github.com/Hans22301/digital-electronics-1/blob/main/labs/project_morse_code_receiver/images/mapa_znaku.png)
	
2. Create source file for our project that would insert buttons entries as zeroes and ones(. = 0 , _ = 1) and shift them into memory.
	
3. Create TOP source file that would use our translate program and our inserting program and with help from seven segment driver and clock enabling program, to show recieved character.
	
![your figure](https://github.com/Hans22301/digital-electronics-1/blob/main/labs/project_morse_code_receiver/images/diagram_proj.png)

<a name="hardware"></a>
## Hardware description

As our hardware we are using board Nexys A7-50t.

![your figure](https://github.com/Hans22301/digital-electronics-1/blob/main/labs/project_morse_code_receiver/images/deska_orig.png)

On this board we will use 4 buttons as our inputs(UP = _, DOWN =., CENTER = ENTER, LEFT = BACKSPACE), 100MHz clock, seven segment display to print out final characters.

<a name="modules"></a>
## VHDL modules description and simulations

**IMPUTT**

This module is created to take button presses, depending on button thats been pressed, the module will assign value (UP will assign 1 and DOWN will assign 0), pressing left button will delete last value(in case of input  mistake) and center button works as enter and will end the input phase of character.

**TRANSLATE**

Translate module works as character map, morse code input will be translated into code input for seven segment display driver and exported to hex_7seg module.

**CLOCK_ENABLE**

This module is exact one we used in previous lectures, because we didnt need to rewrite anything. Its used to create input 100MHz clock signal.

**HEX_7SEG**
This module works very similar to the one we programmed in lecture, but we rewrote it to work for us(added all characters in alphabet) as seen in next picture.

![your figure](https://github.com/Hans22301/digital-electronics-1/blob/main/labs/project_morse_code_receiver/images/mapa_znaku.png)


<a name="top"></a>
## TOP module description and simulations

Write your text here.


<a name="video"></a>
## Video

In the next video we will shortly introduce you to our project.

[YOUTUBE VIDEO](https://github.com/...)

[PRESENTATION](https://vutbr-my.sharepoint.com/:p:/g/personal/xmucha11_vutbr_cz/EfuMuLWZGjlKjdNw_ewh3QQBPMM-HOBnsedU1G0o26pXcA?e=4Flh2b)

<a name="references"></a>
## References

This project was created with help from our past lectures and our brains.

