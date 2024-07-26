 # Digital Clock using Python

This repository contains a simple digital clock application built using Python and the Tkinter library.

## Author

Seth Momanyi

## Description

This project demonstrates how to create a digital clock using Python's Tkinter library. The clock updates every second and displays the current time in hours, minutes, and seconds in a 12-hour format with AM/PM.

## Features

- Displays current time in `HH:MM:SS AM/PM` format
- Updates every second
- Customizable font, background, and foreground colors

## Prerequisites

To run this project, you need to have Python installed on your system. You can download it from the [official Python website](https://www.python.org/downloads/).

## Installation

1. Clone the repository to your local machine:

    ```sh
    git clone https://github.com/i-am-more-manyi/Digital-Clock.git
    ```

2. Navigate to the project directory:

    ```sh
    cd digital-clock
    ```

3. Run the Python script:

    ```sh
    python digital_clock.py
    ```

## Code

```python
from tkinter import *
from tkinter.ttk import *
from time import strftime

root = Tk()
root.title('Digital clock')

def clock():
    tick = strftime('%H:%M:%S %p')
    label.config(text=tick)
    label.after(1000, clock)

label = Label(root, font=('sans', 80), background='black', foreground='red')
label.pack(anchor='center')

clock()
mainloop()

