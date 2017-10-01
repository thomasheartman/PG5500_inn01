# PG5500 Embedded Systems - inn01: LED Matrix

This repo contains everything related to the first assignment in PG500.

## Functionality

The matrix scrolls the text that is defined within the code. The joystick controls the speed and the direction of the text based on user input.

### A note about the joystick

I have chosen to interpret the Y-axis of the joystick as my horizontal controller input simply becuse having the wires facing towards me felt the most natural when working with this. Had joystick been attached to a controller or otherwise had a clearly designated "right way up", using the X-axis would have been a natural choice. However, as I'm only using a single axis and the joystick is free floating, it makes little difference, and the Y-axis was more comfortable to work with.

## Schematics

Please see the attached schematics file for an example of how to wire the project.

### Notes

- In the schematics I have opted to go for two 15kΩ resistors rather than the three 10kΩ I used in the actual setup.
- The attached joystick does not match the version I own, and thus the wiring is not necessarily correct. 5V and GND are correct, of course, but the remaining wire should go from whichever pin send Y-axis information, not necessarily the middle one.

## Video documentation

The video demonstration is available at [this link](http://youtube.com/probably_some_random_numbers)

## Code

### Libraries

I have used the [Bartosz Bielawski's *LEDMatrixDriver*](https://github.com/bartoszbielawski/LEDMatrixDriver) and [Marcello Romani's *SimpleTimer*](https://github.com/marcelloromani/Arduino-SimpleTimer/tree/master/SimpleTimer) libraries to control the matrix and to handle delaying updating without ignoring input respectively.

Both libraries have been very useful, the *LEDMatrixDriver* making connecting and controlling the driver very simple, and the *SimpleTimer* library taking care of all the time control I had the need for.

### Further development

Given more time and a desire to take things further, it would be interesting to look at scrolling text not just from side to side, but also up and down (in particular if you have a multiline sentence).

## Authors

Thomas Hartmann