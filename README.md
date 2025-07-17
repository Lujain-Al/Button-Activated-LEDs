# Button-Activated-LEDs

# Arduino Control Code 

## Overview

This Arduino sketch sets up a basic control system using three input pins and three output pins. Depending on which input pin receives a HIGH signal, the corresponding output pin will be activated, creating a simple signaling system.

## Components Required

- Arduino Board (e.g., Arduino Uno)
- LED lights (3)
- Resistors (220 ohm for LEDs)
- Push buttons or switches (3)
- Breadboard and jumper wires

## Pin Configuration

- **Pin 2**: Input (button/switch 1)
- **Pin 4**: Input (button/switch 2)
- **Pin 7**: Input (button/switch 3)
- **Pin 8**: Output (LED connected to pin 8)
- **Pin 12**: Output (LED connected to pin 12)
- **Pin 13**: Output (LED connected to pin 13)

## Code Explanation

### Setup Function

- Initializes input and output pins using `pinMode()`.
- Input pins are set to `INPUT` mode to read button states.
- Output pins are set to `OUTPUT` mode to control LEDs.

### Loop Function

- Continuously checks the state of the input pins.
- Activates the corresponding LED for 300 milliseconds when a button is pressed:
  - If the button connected to pin 7 is pressed, LED on pin 13 lights up.
  - If the button connected to pin 4 is pressed, LED on pin 12 lights up.
  - If the button connected to pin 2 is pressed, LED on pin 8 lights up.
- If no buttons are pressed, all LEDs remain off.

## Usage

1. Connect the components as per the pin configuration.
2. Upload the code to your Arduino board using the Arduino IDE.
3. Press the buttons to see the corresponding LEDs light up.

## Notes

- Ensure that the buttons are connected correctly with pull-down resistors if necessary.
- Adjust the delay time in the `delay()` function as needed for your application.
