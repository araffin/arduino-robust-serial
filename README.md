# Robust Arduino Serial Protocol

**Robust Arduino Serial** is a simple and robust serial communication protocol. It was designed to make two Arduinos communicate, but can also be useful when you want a computer (e.g. a Raspberry Pi) to communicate with an Arduino.

**Please read the [Medium Article](https://medium.com/@araffin/simple-and-robust-computer-arduino-serial-communication-f91b95596788) to have an overview of this protocol.**

Implementations are available in various programming languages:

- Arduino (`arduino-serial/` folder)
- [Python](https://github.com/araffin/python-arduino-serial)
- [C++](https://github.com/araffin/cpp-arduino-serial)
- [Rust](https://github.com/araffin/rust-arduino-serial)


**Examples** are provided in each repository.

To clone all the repositories at once, tou need to use the `--recursive` command:
```
git clone https://github.com/araffin/arduino-robust-serial.git --recursive
```

### Provided Functions

Please check examples in the different repos to have the parameters details for each programming language.

- `read_order()`: Read one byte from a file/serial port and convert it to an order (equivalent to read_i8)
- `read_i8()`: Read one byte from a file/serial port and convert it to a 8 bits int
- `read_i16()`: Read one byte from a file/serial port and convert it to a 16 bits int
- `read_i32()`: Read one byte from a file/serial port and convert it to a 32 bits int
- `write_order()`: Write an order to a file/serial port. (equivalent to write_i8)
- `write_i8()`: Write one byte int to a file/serial port.
- `write_i16()`: Write two bytes (16-bits) int to a file/serial port.
- `write_i32()`: Write four bytes (32-bits) int to a file/serial port.


### Arduino Implementation

Recommended: Arduino-Makefile
```
sudo apt-get install arduino-mk
```

Compile and upload the code to the Arduino (please check the board name in the Makefile):
```
cd arduino-board/
make
make upload
```

### Python Implementation

[![Build Status](https://travis-ci.org/araffin/python-arduino-serial.svg?branch=master)](https://travis-ci.org/araffin/python-arduino-serial)

Python repository: [https://github.com/araffin/python-arduino-serial](https://github.com/araffin/python-arduino-serial)

### C++ Implementation

[![Build Status](https://travis-ci.org/araffin/cpp-arduino-serial.svg?branch=master)](https://travis-ci.org/araffin/cpp-arduino-serial)


C++ repository: [https://github.com/araffin/cpp-arduino-serial](https://github.com/araffin/cpp-arduino-serial)


### Rust Implementation

[![Build Status](https://travis-ci.org/araffin/rust-arduino-serial.svg?branch=master)](https://travis-ci.org/araffin/rust-arduino-serial) [![Build status](https://ci.appveyor.com/api/projects/status/h0ejgesat0nnpahc/branch/master?svg=true)](https://ci.appveyor.com/project/araffin/rust-arduino-serial/branch/master)

Rust repository: [https://github.com/araffin/rust-arduino-serial](https://github.com/araffin/rust-arduino-serial)

### Real Life Example

This protocol was used on the Racing Robot: [https://github.com/sergionr2/RacingRobot](https://github.com/sergionr2/RacingRobot)

[![The racing robot](https://cdn-images-1.medium.com/max/2000/1*UsmiJ4IzXi6U9svKjB22zw.jpeg)](https://www.youtube.com/watch?v=xhI71ZdSh6k)

### Acknowledgments

I would like to thanks Dara Ly for the original idea of communicating with the Arduino via a command parser, and Xuan Zhang for fixing Arduino limited buffer issue.
