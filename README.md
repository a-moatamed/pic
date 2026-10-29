# GAUN Microcontroller Course Labs & Projects

This repository contains the full semester's laboratory experiments and projects for the Microcontroller course at Gaziantep University (GAUN). The projects are developed for PIC microcontrollers using both C and Assembly languages, compiled via MPLAB X IDE, and designed to be simulated using Proteus.

## Tools & Technologies Used

* **IDE:** MPLAB X IDE


* **Compilers:** XC8 (for C projects) and MPASMWIN (for Assembly projects)


* **Simulation:** Proteus
* **Microcontroller:** PIC Family (e.g., PIC16F/PIC18F series)



## Repository Structure & Project Descriptions

The repository is organized into distinct MPLAB X project folders (`.X`), each covering a specific microcontroller concept or hardware interface:

* **`digital counter.X`**: A digital counter implementation that utilizes Timer1 (`TMR1`) and timer control registers (`T1CON`) for counting and outputs the value to `PORTB`.


* **`7segm.X`**: Interfacing and controlling a 7-segment display.


* **`lcd.X` & `lcd_course.X`**: Projects dedicated to alphanumeric Liquid Crystal Display (LCD) interfacing and control using C.


* **`steppermotor.X`**: Implementation of stepper motor control sequences.


* **`ultrasonic.X`**: Distance measurement utilizing an ultrasonic sensor, featuring trigger and echo pulse timing via `ultrasonic.c` and `counter.c` modules.


* **`ADC_54k22.X`**: Analog-to-Digital Converter (ADC) readings, likely optimized for the PIC18FxxK22 series microcontrollers.


* **`IRQ.X`**: Hardware interrupt request handling. This project configures external interrupts (`INTE`, `INTEDG`) and includes an Interrupt Service Routine (`void __interrupt() ISR()`) to toggle port pins based on interrupt flags.


* **`VU.X`**: A VU (Volume Unit) meter implementation, typically using ADC and an LED bar graph to visualize signal levels.


* **`timer407.X` & `timmerdealy.X`**: Timer configuration projects demonstrating how to generate precise delays without blocking the CPU.


* **`delayAssembly.X`**: Precise delay generation written directly in PIC Assembly (`delay.asm`).


* **`LCDassymbly.X`**: LCD initialization and text rendering written purely in PIC Assembly (`main.asm`).


* **`EXP_5.X`**: Code for laboratory Experiment 5.


* **`407C.X` & `TEE.X`**: Additional course-specific C programming experiments and module tests.



## How to Use

1. **Open a Project:** Launch MPLAB X IDE, select *File > Open Project*, and select any of the `.X` directories (e.g., `digital counter.X`).


2. **Build the Code:** Click the *Build* or *Clean and Build* button. The IDE will compile the C or Assembly code and generate a `.hex` file.
3. **Locate the Hex File:** Once built, the compiled hex files can be found in the project's `dist/default/production/` directory (e.g., `digital_counter.X.production.hex`).


4. **Simulate in Proteus:** Open your Proteus schematic, double-click the PIC microcontroller component, and set the "Program File" property to the newly generated `.hex` file to run the simulation.