# R-pi-Based-audio-reactive-LED-lights
As the name suggest it is a strip of LED lights connected to a Raspberry Pi which acts as the brain of this project which on feeding audio input process the LED light strip such that these lights  fluctuates based on the sound .

## Table of Contents
- [Introduction](#introduction)
- [Required Components](#required-components)
- [Setup Instructions](#setup-instructions)
- [Usage Instructions](#usage-instructions)
- [Conclucion](#Conclucion)

## Introduction
Light up your new year parties and impress all your friends with these amazing music reactive multicolor LED lights that response and change their colors on every loud beat. These lights are nothing but simple RGB LED strips connected to R pi - the brain of this project. LED strips mean that you can mount them anywhere in your home and even outdoors. The only condition is that you have to have an audio output device near your lights to feed them with audio signals which can be processed and reacted upon.

## Required Components
-Raspberry Pi
-LED strip
-Jumper Wires/Connecting Wires
-Audio - Detector sensor 
-LED/Buzzer
-Power Supply

## Setup Instructions
As told above, this project uses an arduino for taking the audio input, processing it and then giving an output through it's digital pins to the LED strip controller circuit which then drives the strips. It uses a 12v power supply to power both the strip and arduino. An advantage of this project is that it doesn't 'waste' any audio jacks. It has an input jack which sends the input signal to arduino and an output jack to send the same signal to your speakers or earphones. The entire project can be completed within 2 hours (or 3 hours maximum) and requires just one of the basic parts that can be found easily. 

## Usage Instructions
Connection: Connect a USB of 3A 5V to your laptop and the other end to the RP2040 Raspberry Pi Pico.
Installation of Thonny: Thonny is an integrated development environment for Python. Install it on your laptop.
Embedding the Code: Open Thonny, connect to the Raspberry Pi Pico, and copy the above Python code into a new file. Save and run the file on the Pico.
Giving Audio Input: After embedding the code, provide audio input to the sound detector. The LEDs will react to the audio input based on the intensity of the sound.

## Conclucion
It   can  be   concluded  from   the  above discussion   that Audio reactive Led lights or Beat sensing lights are a special kind of lights which dances on the intensity of loudness.
 Since these are LED strips, you can mount them almost anywhere by peeling off the 3M tape at the back. So whether you use it as a sofa light or an ambient light on your TV, this thing will spread it's awesomeness everywhere.


## Contributing
Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) for more information.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
